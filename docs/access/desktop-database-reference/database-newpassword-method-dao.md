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
ms.localizationpriority: medium
ms.openlocfilehash: 06658f6c47eb17cb78829c65ce528e565ff69eb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585943"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword メソッド (DAO)

**適用先**: Access 2013、Office 2013

既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .NewPassword(***bstrOld** _, _*_bstrNew_**)

*式* Database オブジェクトを返 **す式** 。

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
<th><p>必須かどうか</p></th>
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
<td><p>Database オブジェクトの <strong>Password</strong> プロパティの新しい <strong>設定</strong> 。</p>
<p><strong>注</strong>: 大文字と小文字、数字、記号を組み合わせた強力なパスワードを使用します。 これらの文字を混在させたものになっていないパスワードは強固とはいえません。 たとえば、Y6dh!et5 は安全性の高いパスワードです。 House27 は推測されやすいパスワードです。 強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

bstrOld 文字列と bstrNew 文字列の長は最大 20 文字で、ASCII 文字 0 (null) を除く任意の文字を含めることができます。 パスワードをクリアするには、bstrNew に長さ 0 の文字列 ("") を使用します。

パスワードでは、大文字と小文字が区別されます。

データベースにパスワードが設定されていない場合は、古いパスワードとして長さ 0 の文字列 ("") が渡され、自動的にパスワードが生成されます。


> [!IMPORTANT]
> [!重要] パスワードを紛失した場合、そのデータベースを二度と開けなくなります。


