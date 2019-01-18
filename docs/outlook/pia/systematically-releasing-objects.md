---
title: オブジェクトを系統的に解放する
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d71ffbdbd10657832a319e1e669f38f311ad99f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708117"
---
# <a name="systematically-releasing-objects"></a>オブジェクトを系統的に解放する

このトピックでは、Outlook を使用するアドイン開発者と IT 管理者向けに、アドインをシャットダウンするときの推奨事項を要約します。詳細については、「[Outlook 2010 でのシャットダウンの変更](https://msdn.microsoft.com/library/ee720183\(v=office.15\))」を参照してください。

## <a name="add-in-shutdown-changes-in-outlook"></a>Outlook アドインのシャットダウンの変更

Outlook 2010 以降の Outlook は、既定ではシャットダウンしているアドインを通知しません。 具体的には、Outlook は、高速シャットダウン時に **IDTExtensibility2** インターフェイスの **OnBeginShutdown(Array)** メソッドおよび **OnDisconnection(ext\_DisconnectMode, Array)** メソッドを呼び出さなくなりました。 同様に、Visual Studio 2010 以降のバージョンの Office 開発ツールで作成した Outlook アドインは、Outlook のシャットダウン中に ThisAddin\_Shutdown メソッドを呼び出さなくなりました。 

これらのメソッドを呼び出さなくなったのは、シャットダウン時に大多数のアドインは参照の解放のような単純なタスクを実行する一方、Web サービスやその他の比較的実行時間の長い処理を同期的に呼び出すアドインも存在するため、Outlook のシャットダウンがかなり遅れることがあったからです。 この変更の結果として、シャットダウン時の動作が以前の Outlook よりも向上しました。

## <a name="recommendations-for-add-in-shutdown-for-developers"></a>アドインのシャットダウンに関する開発者向けの推奨事項

エンド ユーザーが Outlook の高速で応答性の高いシャットダウンを今後も享受できるようにするため、開発者は以下の推奨事項に従う必要があります。

- アドインには、これまでどおりに OnBeginShutdown メソッドと OnDisconnection メソッドまたは ThisAddin\_Shutdown を実装して、参照と割り当てられたメモリを解放するようにしてください。これは、管理者がグループ ポリシーを通じて低速シャットダウンに戻すことや、ユーザーが **[COM アドイン]** ダイアログ ボックスから手動でアドインを切断することがあるためです。

- アドイン開発者は、シャットダウン中に絶対に必要になるタスクのみを実行してください。

- アドイン開発者は、さまざまな状況や、Outlook のシャットダウンを制御するレジストリの設定をいろいろ変えてアドインのパフォーマンスを評価し、Outlook で適切に動作するようにアドインを積極的に修正してください。

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a>アドインのシャットダウンに関する IT 管理者向けの推奨事項

IT 管理者は、既に企業内に展開しているアドインを Outlook の新しいシャットダウン機構と合致するようにアップグレードできない場合、Windows のレジストリの設定をいくつか変更すれば、低速シャットダウンの動作に戻すことができます。

### <a name="individual-add-in-setting"></a>アドインの個別設定

IT 管理者は、アドインの展開の一部として、個別の Outlook アドインへのシャットダウン通知を有効にできます。グループ ポリシーを使用してこれを行うことはできませんが、特定のアドインについて下位互換性が必要な場合に役に立ちます。

この設定は、HKCU または HKLM レジストリ ハイブのアドイン登録で、アドインごとにアドイン登録に値を追加して構成してください。次のテキストを 1 行で入力します。

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

この値を 0x1 に設定すると、アドインは Outlook のシャットダウン時にブロック コールバックを受け取ることができるようになります。これは Outlook のシャットダウンのパフォーマンスに影響するので、使用すべきかどうかを展開の際に評価するようにしてください。この設定を使用するのは、アドインと新しいシャットダウン機構との適合性が特に問題となる場合に限ってください。この値を 0x0 に設定すると、Outlook の既定の動作が使用されます。

### <a name="global-setting"></a>グローバル設定

IT 管理者はグループ ポリシーを使用して、すべてのアドインに対するシャットダウン時の通知をまとめて有効にすることができます。この方法は組織に存在する多数の内部ソリューションやデスクトップでこの設定を展開して、Outlook のロールアウト時に矛盾が生じないようにする必要がある場合に推奨されます。

この設定は、シャットダウン機構の動作を Outlook 2007 と同じにするためのものです。この設定は、ユーザー単位またはコンピューター単位でのグループ ポリシーを通じて、この設定を展開できます。次のテキストを 1 行で入力します。

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

AddinFastShutdownBehavior を 0x1 に設定すると、すべてのアドインのシャットダウン通知が有効になります。この値を 0x0 に設定すると、Outlook の既定の動作が使用されます。

