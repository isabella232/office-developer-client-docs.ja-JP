---
title: CommandType プロパティ (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880237"
---
# <a name="commandtype-property-ado"></a>CommandType プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Command](command-object-ado.md) オブジェクトの型を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。

> [!NOTE]
> [!メモ] **CommandType** では、 **adCmdFile** または **adCmdTableDirect** の **CommandTypeEnum** 値を使用しないでください。これらの値は、 [Recordset](open-method-ado-recordset.md) の [Open](requery-method-ado.md) メソッドと [Requery](recordset-object-ado.md) メソッドのオプションとしてのみ使用することができます。


## <a name="remarks"></a>解説

**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。

**CommandType** プロパティの値が **adCmdUnknown** (既定値) と等しい場合、パフォーマンスが低下することがあります。これは、 **CommandText** プロパティの型が SQL ステートメント、ストアド プロシージャ、またはテーブル名であるかを調べるためにプロバイダーを呼び出す必要があるためです。使っているコマンドの種類がわかっている場合は、 **CommandType** プロパティを設定することにより、該当するコードに直接移動できます。 **CommandType** プロパティが **CommandText** プロパティのコマンドの種類と一致しない場合に [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドを呼び出すと、エラーが発生します。

