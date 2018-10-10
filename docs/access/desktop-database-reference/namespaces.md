---
title: 名前空間 (アクセスのデスクトップのデータベース参照)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc7c0cf302c0b8a297310dfa439ac87724331569
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478362"
---
# <a name="namespaces"></a>名前空間


**適用されます**Access 2013 |。Office 2013

## <a name="namespaces"></a>名前空間

ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>接頭語</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>参照して、 &quot;XML データ&quot;名前空間の要素と現在の<strong>レコード セット</strong>のスキーマを定義する属性が含まれています。</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>データ型定義の仕様を表します。</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>現在の行セットのスキーマを表します。</p></td>
</tr>
</tbody>
</table>


仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。


> [!NOTE]
> <P>[!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。</P>



名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。

## <a name="namespaces"></a>名前空間

ADO での XML の保存形式には、次の 4 つの名前空間が使用されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>接頭語</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>s</p></td>
<td><p>参照して、 &quot;XML データ&quot;名前空間の要素と現在の<strong>レコード セット</strong>のスキーマを定義する属性が含まれています。</p></td>
</tr>
<tr class="even">
<td><p>dt</p></td>
<td><p>データ型定義の仕様を表します。</p></td>
</tr>
<tr class="odd">
<td><p>rs</p></td>
<td><p>ADO の <strong>Recordset</strong> プロパティおよび属性に固有の要素と属性を含む名前空間を表します。</p></td>
</tr>
<tr class="even">
<td><p>z</p></td>
<td><p>現在の行セットのスキーマを表します。</p></td>
</tr>
</tbody>
</table>


仕様に定義されているように、クライアントは独自のタグをこれらの名前空間に追加することはできません。たとえば、クライアントは名前空間を "urn:schemas-microsoft-com:rowset" として定義し、"rs:MyOwnTag" などを書き込むことはできません。名前空間の詳細については、「[XML 名前空間 (英語)](https://www.w3.org/tr/xml-names/)」を参照してください。


> [!NOTE]
> <P>[!メモ] スキーマ タグの ID は "RowsetSchema" であることが必要です。また、現在の行セットのスキーマを表すために使用される名前空間は、"#RowsetSchema" を指す必要があります。</P>



名前空間のプレフィックス (コロンの右側で等号の左側の部分) は任意です。

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

この名前が XML ドキュメント全体で一貫して使用される限り、ユーザーはこれを任意の名前に定義できます。ADO は常に "s"、"rs"、"dt"、および "z" を書き込みますが、これらのプレフィックス名は、読み込むコンポーネント内にはハードコーディングされません。

