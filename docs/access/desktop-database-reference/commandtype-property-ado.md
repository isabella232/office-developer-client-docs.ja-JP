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
localization_priority: Normal
ms.openlocfilehash: c978a6a227266fa43c1102fc109be2b81262de8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296123"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="8d714-102">CommandType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8d714-102">CommandType property (ADO)</span></span>


<span data-ttu-id="8d714-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d714-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d714-104">[Command](command-object-ado.md) オブジェクトの型を示します。</span><span class="sxs-lookup"><span data-stu-id="8d714-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8d714-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="8d714-105">Settings and return values</span></span>

<span data-ttu-id="8d714-106">1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="8d714-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="8d714-p101">[!メモ] **CommandType** では、 **adCmdFile** または **adCmdTableDirect** の **CommandTypeEnum** 値を使用しないでください。これらの値は、 [Recordset](open-method-ado-recordset.md) の [Open](requery-method-ado.md) メソッドと [Requery](recordset-object-ado.md) メソッドのオプションとしてのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8d714-p101">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**. These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="8d714-109">注釈</span><span class="sxs-lookup"><span data-stu-id="8d714-109">Remarks</span></span>

<span data-ttu-id="8d714-110">**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8d714-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="8d714-p102">**CommandType** プロパティの値が **adCmdUnknown** (既定値) と等しい場合、パフォーマンスが低下することがあります。これは、 **CommandText** プロパティの型が SQL ステートメント、ストアド プロシージャ、またはテーブル名であるかを調べるためにプロバイダーを呼び出す必要があるためです。使っているコマンドの種類がわかっている場合は、 **CommandType** プロパティを設定することにより、該当するコードに直接移動できます。 **CommandType** プロパティが **CommandText** プロパティのコマンドの種類と一致しない場合に [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d714-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

