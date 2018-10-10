---
title: カスタマイズ ファイルの Logs セクション
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478991"
---
# <a name="customization-file-logs-section"></a>カスタマイズ ファイルの Logs セクション

**適用されます**Access 2013 |。Office 2013

**logs** セクションには、 **DataFactory** の操作中に発生したエラーを記録するファイル名を指定する、ログ ファイル エントリを含めます。

## <a name="syntax"></a>構文

ログ ファイル エントリの形式は、次のとおりです。

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>これがログ ファイル エントリであることを示すリテラル文字列。</p></td>
</tr>
<tr class="even">
<td><p><em>Filename</em></p></td>
<td><p>完全パスとファイル名。通常のファイル名は、<strong>c:\msdfmap.log</strong> です。</p></td>
</tr>
</tbody>
</table>


ログ ファイルには、各エラーのユーザー名、HRESULT、および発生日時が含まれます。

