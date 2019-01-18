---
title: Database.NewPassword メソッド (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708670"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword メソッド (DAO)

**適用されます**Access 2013、Office 2013。

既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。NewPassword (***bstrOld***、 ***bstrNew***)

*式***データベース**オブジェクトを返すオブジェクト式を指定します。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>bstrOld</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Database</strong> オブジェクトの <strong>Password</strong> プロパティの現在の設定値。</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Database</strong>オブジェクトの<strong>Password</strong>プロパティの新しい設定します。</p>
<p><strong>注</strong>: 大文字と小文字の英字、数字、および記号を組み合わせた強力なパスワードを使用します。 これらの文字を混在させたものになっていないパスワードは強固とはいえません。 たとえば、Y6dh!et5 は安全性の高いパスワードです。 House27 は推測されやすいパスワードです。 また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

BstrOld および bstrNew の文字列は、長さは最大 20 文字し、ASCII 文字 0 (null) 以外の任意の文字を含めることができます。 パスワードをクリアするには、長さ 0 の文字列を使用します ("") bstrNew のです。

パスワードでは、大文字と小文字が区別されます。

データベースにパスワードが設定されていない場合は、古いパスワードとして長さ 0 の文字列 ("") が渡され、自動的にパスワードが生成されます。


> [!IMPORTANT]
> [!重要] パスワードを紛失した場合、そのデータベースを二度と開けなくなります。


