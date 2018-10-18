---
title: Optimize プロパティ -- 動的 (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605178"
---
# <a name="optimize-property--dynamic-ado"></a>Optimize プロパティ -- 動的 (ADO)


**適用されます**Access 2013 |。Office 2013

フィールドにインデックスを作成するかどうかを指定します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

インデックスを作成するかどうかを表すブール型 ( **Boolean** ) の値を設定または取得します。

## <a name="remarks"></a>解説

インデックスを使用すると、[Recordset](recordset-object-ado.md) の値の検索や並べ替えのパフォーマンスが向上します。インデックスは ADO 内部の機能であり、アプリケーション内で明示的にアクセスしたり使用したりすることはできません。

フィールドにインデックスを作成するには、 **Optimize** プロパティを **True** に設定します。インデックスを削除するには、このプロパティを **False** に設定します。

**Optimize** は、 [CursorLocation](field-object-ado.md) プロパティが [adUseClient](properties-collection-ado.md) に設定されているときに [Field](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

**使用例**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
