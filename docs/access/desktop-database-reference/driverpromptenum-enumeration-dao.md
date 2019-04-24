---
title: DriverPromptEnum 列挙 (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293666"
---
# <a name="driverpromptenum-enumeration-dao"></a>DriverPromptEnum 列挙 (DAO)


**適用先:** Access 2013、Office 2013

ユーザーに接続を確立するための確認のメッセージを表示するかどうか、またいつ表示するかを指定します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbDriverComplete</p></td>
<td><p>.0</p></td>
<td><p>指定された接続文字列に DSN キーワードが含まれている場合、ドライバー マネージャーはその文字列を接続でそのまま使用します。それ以外の場合は、<strong>dbDriverPrompt</strong> が指定されたときと同じように動作します。</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>1/3</p></td>
<td><p>(既定値) <strong>dbDriverComplete</strong> が指定されたときと同じように動作します。ただし、ドライバーは接続を完了するために必要ではないすべての情報のためのコントロールを無効にします。</p></td>
</tr>
<tr class="odd">
<td><p>dbdrivernoprompt</p></td>
<td><p>1-d</p></td>
<td><p>ドライバー マネージャーは指定された接続文字列を接続で使用します。十分な情報が指定されていない場合は、トラップ可能なエラーが返されます。</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>pbm-2</p></td>
<td><p>ドライバー マネージャーは [<strong>接続する ODBC データ ソース</strong>] ダイアログ ボックスを表示します。接続の確立に使用される接続文字列は、このダイアログ ボックスを通じてユーザーが選択および完成させたデータ ソース名 (DSN) から構築されます。</p></td>
</tr>
</tbody>
</table>

