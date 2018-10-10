---
title: Value プロパティ (ADO)
TOCTitle: Value Property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68c0d45345dfc768f5d435689abf67bcc3d9abe2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476445"
---
# <a name="value-property-ado"></a><span data-ttu-id="08c01-102">Value プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="08c01-102">Value Property (ADO)</span></span>


<span data-ttu-id="08c01-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="08c01-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08c01-104">[Field](field-object-ado.md) オブジェクト、 [Parameter](parameter-object-ado.md) オブジェクト、または [Property](property-object-ado.md) オブジェクトに割り当てられた値を示します。</span><span class="sxs-lookup"><span data-stu-id="08c01-104">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="08c01-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="08c01-105">Settings and Return Values</span></span>

<span data-ttu-id="08c01-p101">オブジェクトの値を示すバリアント型 ( **Variant** ) の値を設定または取得します。既定値は [Type](type-property-ado.md) プロパティによって異なります。</span><span class="sxs-lookup"><span data-stu-id="08c01-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c01-108">解説</span><span class="sxs-lookup"><span data-stu-id="08c01-108">Remarks</span></span>

<span data-ttu-id="08c01-p102">**Field** オブジェクトのデータを設定または取得するとき、 **Parameter** オブジェクトでパラメーター値を設定または取得するとき、または **Property** オブジェクトでプロパティを設定または取得するときには、 **Value** プロパティを使用します。 **Value** プロパティは、さまざまな要因によって、値の取得と設定が可能な場合と、値の取得のみが可能な場合があります。詳細については、各オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="08c01-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="08c01-111">ADO では、 **Value** プロパティを使用してロング バイナリ データを設定および取得できます。</span><span class="sxs-lookup"><span data-stu-id="08c01-111">ADO allows setting and returning long binary data with the **Value** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="08c01-p103">[!メモ] <STRONG>Parameter</STRONG> オブジェクトの場合、ADO はプロバイダーから一度だけ <STRONG>Value</STRONG> プロパティを取得します。コマンドに含まれる <STRONG>Parameter</STRONG> の <STRONG>Value</STRONG> プロパティが空で、このコマンドから <A href="recordset-object-ado.md">Recordset</A> を作成する場合は、 <STRONG>Value</STRONG> プロパティを取得する前に、 <STRONG>Recordset</STRONG> を閉じる必要があります。このようにしないと、プロバイダーによっては、 <STRONG>Value</STRONG> プロパティが空になり、正しい値が格納されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="08c01-p103">For <STRONG>Parameter</STRONG> objects, ADO reads the <STRONG>Value</STRONG> property only once from the provider. If a command contains a <STRONG>Parameter</STRONG> whose <STRONG>Value</STRONG> property is empty, and you create a <A href="recordset-object-ado.md">Recordset</A> from the command, ensure that you first close the <STRONG>Recordset</STRONG> before retrieving the <STRONG>Value</STRONG> property. Otherwise, for some providers, the <STRONG>Value</STRONG> property may be empty, and won't contain the correct value.</span></span></P>



<span data-ttu-id="08c01-p104">**Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションに新しい [Field](record-object-ado.md) オブジェクトを追加した場合は、 **Value** プロパティを最初に設定してから、他の **Field** プロパティを指定する必要があります。まず、 **Value** プロパティに特定の値を割り当て、 [Fields](update-method-ado.md) コレクションで **Update** を呼び出します。その後は、 [Type](type-property-ado.md) や [Attributes](attributes-property-ado.md) などの他のプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="08c01-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

