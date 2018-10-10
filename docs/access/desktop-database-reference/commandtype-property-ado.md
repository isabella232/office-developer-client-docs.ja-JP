---
title: CommandType プロパティ (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479676"
---
# <a name="commandtype-property-ado"></a>CommandType プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Command](command-object-ado.md) オブジェクトの型を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。


> [!NOTE]
> <P>[!メモ] <STRONG>CommandType</STRONG> では、 <STRONG>adCmdFile</STRONG> または <STRONG>adCmdTableDirect</STRONG> の <STRONG>CommandTypeEnum</STRONG> 値を使用しないでください。これらの値は、 <A href="open-method-ado-recordset.md">Recordset</A> の <A href="requery-method-ado.md">Open</A> メソッドと <A href="recordset-object-ado.md">Requery</A> メソッドのオプションとしてのみ使用することができます。</P>



## <a name="remarks"></a>解説

**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。

**CommandType** プロパティの値が **adCmdUnknown** (既定値) と等しい場合、パフォーマンスが低下することがあります。これは、 **CommandText** プロパティの型が SQL ステートメント、ストアド プロシージャ、またはテーブル名であるかを調べるためにプロバイダーを呼び出す必要があるためです。使っているコマンドの種類がわかっている場合は、 **CommandType** プロパティを設定することにより、該当するコードに直接移動できます。 **CommandType** プロパティが **CommandText** プロパティのコマンドの種類と一致しない場合に [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) メソッドを呼び出すと、エラーが発生します。

