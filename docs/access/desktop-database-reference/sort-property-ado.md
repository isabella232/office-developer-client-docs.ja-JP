---
title: Sort プロパティ (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 62ac60b1c7575f0b0d3e003dc58a11fe4d86c131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308639"
---
# <a name="sort-property-ado"></a>Sort プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

**Recordset** の並べ替えに使用するフィールド名を示す文字列型 ( **String** ) の値を設定または取得します。各フィールド名はコンマで区切って指定し、フィールド名に続けて空白およびキーワードとして、フィールドを昇順で並べ替えることを示す **ASC** または降順で並べ替えることを示す **DESC** を指定できます。既定では、キーワードを指定しなかった場合、フィールドは昇順に並べ替えられます。

## <a name="remarks"></a>注釈

このプロパティを使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティが **adUseClient** に設定されている必要があります。インデックスが存在しない場合は、 **Sort** プロパティで指定した各フィールドについて一時インデックスが作成されます。

並べ替え処理では、データは物理的に並べ替えられるわけではなく、インデックスで指定された順序でアクセスされるだけなので効率的です。

**Sort** プロパティを空の文字列に設定すると、行は元の順序にリセットされ、一時インデックスは削除されます。既存のインデックスは削除されません。

**Recordset** に、*firstName* (名)、*middleInitial* (ミドルネームのイニシャル)、および *lastName* (姓) という名前の 3 つのフィールドがあるとします。 並べ替えプロパティを文字列 "lastName DESC, firstName ASC" に設定します。これにより、**レコードセット**は姓で降順に並べ替えられ、次に先頭の名前が昇順で**並べ替え**られます。 ミドルネームのイニシャルは無視されます。

"ASC" または "DESC" というフィールド名は、キーワード **ASC** および **DESC** と競合するので使用できません。名前が競合する場合は、 **Recordset** を返すクエリで **AS** キーワードを使用して、名前が競合するフィールドに別名を指定します。

