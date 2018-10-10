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
# <a name="commandtype-property-ado"></a><span data-ttu-id="6d23a-102">CommandType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="6d23a-102">CommandType Property (ADO)</span></span>


<span data-ttu-id="6d23a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d23a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d23a-104">[Command](command-object-ado.md) オブジェクトの型を示します。</span><span class="sxs-lookup"><span data-stu-id="6d23a-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6d23a-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="6d23a-105">Settings and Return Values</span></span>

<span data-ttu-id="6d23a-106">1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6d23a-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d23a-p101">[!メモ] <STRONG>CommandType</STRONG> では、 <STRONG>adCmdFile</STRONG> または <STRONG>adCmdTableDirect</STRONG> の <STRONG>CommandTypeEnum</STRONG> 値を使用しないでください。これらの値は、 <A href="open-method-ado-recordset.md">Recordset</A> の <A href="requery-method-ado.md">Open</A> メソッドと <A href="recordset-object-ado.md">Requery</A> メソッドのオプションとしてのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6d23a-p101">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>. These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="6d23a-109">解説</span><span class="sxs-lookup"><span data-stu-id="6d23a-109">Remarks</span></span>

<span data-ttu-id="6d23a-110">**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6d23a-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="6d23a-p102">**CommandType** プロパティの値が **adCmdUnknown** (既定値) と等しい場合、パフォーマンスが低下することがあります。これは、 **CommandText** プロパティの型が SQL ステートメント、ストアド プロシージャ、またはテーブル名であるかを調べるためにプロバイダーを呼び出す必要があるためです。使っているコマンドの種類がわかっている場合は、 **CommandType** プロパティを設定することにより、該当するコードに直接移動できます。 **CommandType** プロパティが **CommandText** プロパティのコマンドの種類と一致しない場合に [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6d23a-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

