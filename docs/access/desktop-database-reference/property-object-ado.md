---
title: Property オブジェクト (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fe6ac64417c5758d25872a7b67be7cb9f12ac6d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874510"
---
# <a name="property-object-ado"></a><span data-ttu-id="fd329-102">Property オブジェクト (ADO)</span><span class="sxs-lookup"><span data-stu-id="fd329-102">Property Object (ADO)</span></span>


<span data-ttu-id="fd329-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fd329-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd329-104">プロバイダーで定義される ADO オブジェクトの動的特性を表します。</span><span class="sxs-lookup"><span data-stu-id="fd329-104">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd329-105">備考</span><span class="sxs-lookup"><span data-stu-id="fd329-105">Remarks</span></span>

<span data-ttu-id="fd329-106">ADO オブジェクトには、組み込みのプロパティと動的プロパティという 2 種類のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="fd329-106">ADO objects have two types of properties: built-in and dynamic.</span></span>

<span data-ttu-id="fd329-107">組み込みのプロパティは、これらのプロパティは、ADO に実装されていると、構文を使用して、すべての新しいオブジェクトにすぐに利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fd329-107">Built-in properties are those properties implemented in ADO and immediately available to any new object, using the syntax.</span></span> <span data-ttu-id="fd329-108">これらのプロパティは、オブジェクトの **Properties** コレクション内の [Property](properties-collection-ado.md) オブジェクトとして格納されないため、値の変更はできますが、特性を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fd329-108">They do not appear as **Property** objects in an object's [Properties](properties-collection-ado.md) collection, so although you can change their values, you cannot modify their characteristics.</span></span>

<span data-ttu-id="fd329-109">動的プロパティは、基になるデータ プロバイダーによって定義され、該当する ADO オブジェクトの **Properties** コレクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd329-109">Dynamic properties are defined by the underlying data provider, and appear in the **Properties** collection for the appropriate ADO object.</span></span> <span data-ttu-id="fd329-110">たとえば、プロバイダー固有のプロパティには、 [Recordset](recordset-object-ado.md) オブジェクトがトランザクションや更新をサポートしているかどうかを示すものがあります。</span><span class="sxs-lookup"><span data-stu-id="fd329-110">For example, a property specific to the provider may indicate if a [Recordset](recordset-object-ado.md) object supports transactions or updating.</span></span> <span data-ttu-id="fd329-111">これらの追加のプロパティは、その **Recordset** オブジェクトの **Properties** コレクションに、 **Property** オブジェクトとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="fd329-111">These additional properties will appear as **Property** objects in that **Recordset** object's **Properties** collection.</span></span> <span data-ttu-id="fd329-112">動的プロパティは、MyObject.Properties(0) を使用して、このコレクションを通じてのみ参照できるか、または MyObject.Properties("Name") の構文です。</span><span class="sxs-lookup"><span data-stu-id="fd329-112">Dynamic properties can be referenced only through the collection, using the MyObject.Properties(0) or or MyObject.Properties("Name") syntax.</span></span>

<span data-ttu-id="fd329-113">どちらの種類のプロパティも削除できません。</span><span class="sxs-lookup"><span data-stu-id="fd329-113">You cannot delete either kind of property.</span></span>

<span data-ttu-id="fd329-114">動的プロパティである **Property** オブジェクトには、それ自体に次の 4 つの組み込みのプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="fd329-114">A dynamic **Property** object has four built-in properties of its own:</span></span>

  - <span data-ttu-id="fd329-115">[Name](name-property-ado.md) プロパティは、プロパティを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="fd329-115">The [Name](name-property-ado.md) property is a string that identifies the property.</span></span>

  - <span data-ttu-id="fd329-116">[Type](type-property-ado.md) プロパティは、プロパティのデータ型を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="fd329-116">The [Type](type-property-ado.md) property is an integer that specifies the property data type.</span></span>

  - <span data-ttu-id="fd329-p103">[Value](value-property-ado.md) プロパティは、プロパティの設定を格納する変数です。 **Value** は、 **Property** オブジェクトの既定のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="fd329-p103">The [Value](value-property-ado.md) property is a variant that contains the property setting. **Value** is the default property for a **Property** object.</span></span>

  - <span data-ttu-id="fd329-119">[Attributes](attributes-property-ado.md) プロパティは、プロバイダー固有のプロパティの特性を示す長整数型 (Long) の値です。</span><span class="sxs-lookup"><span data-stu-id="fd329-119">The [Attributes](attributes-property-ado.md) property is a long value that indicates characteristics of the property specific to the provider.</span></span>

