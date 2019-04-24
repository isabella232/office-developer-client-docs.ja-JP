---
title: RunApplication マクロ アクション
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306840"
---
# <a name="runapplication-macro-action"></a>RunApplication マクロ アクション

**適用先:** Access 2013、Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティ メモ" alt="Security note" /><strong>セキュリティに関するメモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>実行可能ファイルまたはマクロやアプリケーションのコードを実行するときは注意が必要です。実行可能ファイルまたはコードを使用してアクションを実行すると、コンピューターおよびデータのセキュリティを損なうおそれがあります。</td>
</tr>
</tbody>
</table>

You can use the **RunApplication** action to run a Microsoft Windows-based or MS-DOS-based application, such as Microsoft Excel, Microsoft Word, or Microsoft PowerPoint, from within Microsoft Access. For example, you may want to paste Excel spreadsheet data into your Access database.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>設定値

"RunApplication/アプリケーションの実行" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Command Line/コマンド ライン</strong></p></td>
<td><p>アプリケーションの起動に使用するコマンド ラインを指定します。パスの指定や、特定のモードでアプリケーションを実行するスイッチなどのパラメーターの指定もできます。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>コマンド ライン</strong>] ボックスにコマンド ラインを入力します。この引数は省略できません。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションで指定したアプリケーションは、画面の一番手前で起動します。このアクションが定義されているマクロは、アプリケーションの起動後も継続して実行されます。

You can transfer data between the other application and Access by using the Microsoft Windows dynamic data exchange (DDE) facility or the Clipboard. You can use the **SendKeys** action to send keystrokes to the other application (although DDE is a more efficient method for transferring data). You can also share data among applications by using automation.

MS-DOS ベースのアプリケーションは、Windows 環境の MS-DOS ウィンドウで実行します。

Windows オペレーティング システムでは、エクスプローラーからプログラムを起動する方法、[ **スタート**] メニューの [ **ファイル名を指定して実行**] コマンドを使用する方法、Windows のデスクトップでプログラム アイコンをダブルクリックする方法など、さまざまな方法でアプリケーションを実行できます。

You can't run the **RunApplication** action in a Visual Basic for Applications (VBA) module. Use the VBA **Shell** function instead.

