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
ms.openlocfilehash: 4b3d4d26a194e2790bf03fcdc5d1911c1e69bbf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882869"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword メソッド (DAO)


**適用されます**Access 2013、Office 2013。

既存の Microsoft Access データベース エンジンのデータベースのパスワードを変更します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。NewPassword (***bstrOld***、 ***bstrNew***)

*式***データベース**オブジェクトを返すオブジェクト式を指定します。

### <a name="parameters"></a>パラメーター

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
<td><p>bstrOld</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p><strong>Database</strong> オブジェクトの <strong>Password</strong> プロパティの現在の設定値。</p></td>
</tr>
<tr class="even">
<td><p>bstrNew</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p><strong>Database</strong>オブジェクトの<strong>Password</strong>プロパティの新しい設定します。</p>

> [!NOTE]
> 大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

BstrOld および bstrNew の文字列は、長さは最大 20 文字し、ASCII 文字 0 (null) 以外の任意の文字を含めることができます。 パスワードをクリアするには、長さ 0 の文字列を使用します ("") bstrNew のです。

パスワードでは、大文字と小文字が区別されます。

データベースにパスワードが設定されていない場合は、古いパスワードとして長さ 0 の文字列 ("") が渡され、自動的にパスワードが生成されます。


> [!IMPORTANT]
> [!重要] パスワードを紛失した場合、そのデータベースを二度と開けなくなります。


