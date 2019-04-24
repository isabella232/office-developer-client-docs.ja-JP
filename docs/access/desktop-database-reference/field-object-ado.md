---
title: Field オブジェクト-ActiveX データオブジェクト (ADO)
TOCTitle: Field object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2bf17029a706ad6902a8a01a14e73183f94d7a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293057"
---
# <a name="field-object-ado"></a><span data-ttu-id="31fe2-102">Field オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="31fe2-102">Field object (ADO)</span></span>


<span data-ttu-id="31fe2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="31fe2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31fe2-104">共通のデータ型を持つデータの列を表します。</span><span class="sxs-lookup"><span data-stu-id="31fe2-104">Represents a column of data with a common data type.</span></span>

## <a name="remarks"></a><span data-ttu-id="31fe2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="31fe2-105">Remarks</span></span>

<span data-ttu-id="31fe2-p101">各 **Field** オブジェクトは、 [Recordset](recordset-object-ado.md) の 1 つの列に対応します。 [Field](value-property-ado.md) オブジェクトの **Value** プロパティを使用すると、カレント レコードのデータを設定または取得できます。プロバイダーが公開している機能によっては、 **Field** オブジェクトの一部のコレクション、メソッド、またはプロパティを使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="31fe2-p101">Each **Field** object corresponds to a column in the [Recordset](recordset-object-ado.md). You use the [Value](value-property-ado.md) property of **Field** objects to set or return data for the current record. Depending on the functionality the provider exposes, some collections, methods, or properties of a **Field** object may not be available.</span></span>

<span data-ttu-id="31fe2-109">**Field** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-109">With the collections, methods, and properties of a **Field** object, you can do the following:</span></span>

  - <span data-ttu-id="31fe2-110">[Name](name-property-ado.md) プロパティを使用して、フィールドの名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-110">Return the name of a field with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="31fe2-p102">**Value** プロパティを使用して、フィールド内のデータを表示または変更できます。 **Value** は、 **Field** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="31fe2-p102">View or change the data in the field with the **Value** property. **Value** is the default property of the **Field** object.</span></span>

  - <span data-ttu-id="31fe2-113">[Type](type-property-ado.md)、[Precision](precision-property-ado.md)、および [NumericScale](numericscale-property-ado.md) の各プロパティを使用して、フィールドの基本的な特性を取得できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-113">Return the basic characteristics of a field with the [Type](type-property-ado.md), [Precision](precision-property-ado.md), and [NumericScale](numericscale-property-ado.md) properties.</span></span>

  - <span data-ttu-id="31fe2-114">[DefinedSize](definedsize-property-ado.md) プロパティを使用して、フィールドの宣言されたサイズを取得できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-114">Return the declared size of a field with the [DefinedSize](definedsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="31fe2-115">[ActualSize](actualsize-property-ado.md) プロパティを使用して、特定のフィールドに含まれるデータの実際のサイズを取得できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-115">Return the actual size of the data in a given field with the [ActualSize](actualsize-property-ado.md) property.</span></span>

  - <span data-ttu-id="31fe2-116">[Attributes](attributes-property-ado.md) プロパティおよび [Properties](properties-collection-ado.md) コレクションを使用して、特定のフィールドについてサポートされている機能の種類を確認できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-116">Determine what types of functionality are supported for a given field with the [Attributes](attributes-property-ado.md) property and [Properties](properties-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="31fe2-117">[AppendChunk](appendchunk-method-ado.md) メソッドおよび [GetChunk](getchunk-method-ado.md) メソッドを使用して、長いバイナリ データまたは長い文字データを含むフィールドの値を操作できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-117">Manipulate the values of fields containing long binary or long character data with the [AppendChunk](appendchunk-method-ado.md) and [GetChunk](getchunk-method-ado.md) methods.</span></span>

  - <span data-ttu-id="31fe2-118">プロバイダーがバッチ更新をサポートしている場合は、[OriginalValue](originalvalue-property-ado.md) プロパティおよび [UnderlyingValue](underlyingvalue-property-ado.md) プロパティを使用して、バッチ更新中に発生するフィールドの値の不一致を解決できます。</span><span class="sxs-lookup"><span data-stu-id="31fe2-118">If the provider supports batch updates, resolve discrepancies in field values during batch updating with the [OriginalValue](originalvalue-property-ado.md) and [UnderlyingValue](underlyingvalue-property-ado.md) properties.</span></span>

<span data-ttu-id="31fe2-p103">メタデータ プロパティのすべて (**Name**、**Type**、**DefinedSize**、**Precision**、および **NumericScale**) は、**Field** オブジェクトの **Recordset** を開く前に使用可能になります。この時点でこれらのプロパティを設定すると、フォームを動的に作成する際に便利です。</span><span class="sxs-lookup"><span data-stu-id="31fe2-p103">All of the metadata properties (**Name**, **Type**, **DefinedSize**, **Precision**, and **NumericScale**) are available before opening the **Field** object's **Recordset**. Setting them at that time is useful for dynamically constructing forms.</span></span>

