---
title: Value プロパティ (ADO)
TOCTitle: Value property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 00b82706d934356621ac1e41fffca61ec88e081f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305895"
---
# <a name="value-property-ado"></a><span data-ttu-id="30d2b-102">Value プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="30d2b-102">Value property (ADO)</span></span>

<span data-ttu-id="30d2b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="30d2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30d2b-104">[Field](field-object-ado.md) オブジェクト、 [Parameter](parameter-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトに割り当てられた値を示します。</span><span class="sxs-lookup"><span data-stu-id="30d2b-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="30d2b-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="30d2b-105">Settings and return values</span></span>

<span data-ttu-id="30d2b-106">オブジェクトの値を示すバリアント型 ( **Variant** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="30d2b-106">Sets or returns a **Variant** value that indicates the value of the object.</span></span> <span data-ttu-id="30d2b-107">既定値は [Type](type-property-ado.md) プロパティによって異なります。</span><span class="sxs-lookup"><span data-stu-id="30d2b-107">Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="30d2b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="30d2b-108">Remarks</span></span>

<span data-ttu-id="30d2b-p102">**Field** オブジェクトのデータを設定または取得するとき、**Parameter** オブジェクトでパラメーター値を設定または取得するとき、または **Property** オブジェクトでプロパティを設定または取得するときには、**Value** プロパティを使用します。**Value** プロパティは、さまざまな要因によって、値の取得と設定が可能な場合と、値の取得のみが可能な場合があります。詳細については、各オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30d2b-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="30d2b-111">ADO では、 **Value** プロパティを使用してロング バイナリ データを設定および取得できます。</span><span class="sxs-lookup"><span data-stu-id="30d2b-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>

> [!NOTE]
> <span data-ttu-id="30d2b-p103">[!メモ] **Parameter** オブジェクトの場合、ADO はプロバイダーから一度だけ **Value** プロパティを取得します。コマンドに含まれる **Parameter** の **Value** プロパティが空で、このコマンドから [Recordset](recordset-object-ado.md) を作成する場合は、 **Value** プロパティを取得する前に、 **Recordset** を閉じる必要があります。このようにしないと、プロバイダーによっては、 **Value** プロパティが空になり、正しい値が格納されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="30d2b-p103">For **Parameter** objects, ADO reads the **Value** property only once from the provider. If a command contains a **Parameter** whose **Value** property is empty, and you create a [Recordset](recordset-object-ado.md) from the command, ensure that you first close the **Recordset** before retrieving the **Value** property. Otherwise, for some providers, the **Value** property may be empty, and won't contain the correct value.</span></span>

<span data-ttu-id="30d2b-p104">**Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションに新しい [Field](record-object-ado.md) オブジェクトを追加した場合は、 **Value** プロパティを最初に設定してから、他の **Field** プロパティを指定する必要があります。まず、 **Value** プロパティに特定の値を割り当て、 [Fields](update-method-ado.md) コレクションで **Update** を呼び出します。その後は、 [Type](type-property-ado.md) や [Attributes](attributes-property-ado.md) などの他のプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="30d2b-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

