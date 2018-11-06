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
ms.openlocfilehash: caa22f142062b929b2520d5a2de69f9ccddb2145
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998680"
---
# <a name="runapplication-macro-action"></a>RunApplication マクロ アクション

**適用されます**Access 2013、Office 2013。

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><strong>セキュリティ メモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>実行可能ファイルまたはマクロやアプリケーションのコードを実行するときは注意が必要です。実行可能ファイルまたはコードを使用してアクションを実行すると、コンピューターおよびデータのセキュリティを損なうおそれがあります。</td>
</tr>
</tbody>
</table>

**RunApplication**アクションを使用すると、Microsoft access から Microsoft Excel、Word、または Microsoft PowerPoint など、Windows ベースまたは ms-dos アプリケーションを実行します。 たとえば、Excel スプレッドシートのデータを Access データベースに貼り付ける可能性があります。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

**RunApplication**アクションには、次の引数があります。

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


## <a name="remarks"></a>解説

このアクションで指定したアプリケーションは、画面の一番手前で起動します。このアクションが定義されているマクロは、アプリケーションの起動後も継続して実行されます。

他のアプリケーションと Access の間でデータを転送するには、Windows のダイナミック データ エクス (チェンジ DDE) 機能やクリップボードを使用します。 **"キー送信"** アクションを使用すると、(ただし、DDE は、データを転送するためのより効率的な方法です)、その他のアプリケーションにキーストロークを送信します。 オートメーションを使用してアプリケーション間でデータを共有することもできます。

MS-DOS ベースのアプリケーションは、Windows 環境の MS-DOS ウィンドウで実行します。

Windows オペレーティング システムでは、エクスプローラーからプログラムを起動する方法、[ **スタート**] メニューの [ **ファイル名を指定して実行**] コマンドを使用する方法、Windows のデスクトップでプログラム アイコンをダブルクリックする方法など、さまざまな方法でアプリケーションを実行できます。

Visual Basic for Applications (VBA) モジュールでは、 **RunApplication**アクションを実行することはできません。 VBA **Shell**関数を使用してください。

