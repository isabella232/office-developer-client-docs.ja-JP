---
title: コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c155fed72a314c5c260ed2fe574474afd45c44c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406653"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a>コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する

クイック実行は、Office 2010 以降のバージョンで利用できるソフトウェアの配信と更新のメカニズムです。クイック実行で配信された製品は、ローカル オペレーティング システム上の仮想アプリケーション環境で実行されます。つまり、それらの製品は独自のファイルと設定のプライベート コピーを持ち、それらが行った変更は仮想環境内に格納されます。

クイック実行は高速です。ユーザーは、製品全体のインストールが完了するまで待機することなく、短時間のうちにアプリケーションの実行を開始できます。 更新プログラムはバックグラウンドで自動的に実行されます。ユーザーが、最初にインストールを削除する必要や、手動で更新プログラムをインストールする必要はありません。 クイック実行の製品は仮想化されていて、インストール済みの別のソフトウェアと競合することはありません。 ただし、クイック実行で配信される製品には、その製品のすべてのファイルと登録のプライベート コピーがあるため、アドインの開発者は、クライアント コンピューターのハード ディスクにインストールされていた製品と同じ方法では、その製品が存在しているかどうかを判断できません。 Outlook 2010 以降、アドインの開発者は、Outlook がインストールされているかどうかと、Outlook がクイック実行製品として配信されたものかどうかを確認する必要があります。


> [!NOTE]
> [!メモ] クイック実行仮想アプリケーション環境でサポートされるのは 32 ビットの Office 2013 だけです。このことは、クライアント コンピューターで 64 ビットのオペレーティング システムを実行しているとしても変わりません。



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a>Outlook 2013 がクイック実行でクライアント コンピューターに配信されたものかどうかを確認するには

- Windows レジストリ内の次の場所に VirtualOutlook キーが存在するかどうかを確認します。
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  VirtualOutlook キーは REG\_SZ 値です。この値には、インストールされている製品の言語のカルチャ タグ ("en-us" など) が含まれています。

## <a name="see-also"></a>関連項目

- [アドイン管理](add-in-administration.md)

