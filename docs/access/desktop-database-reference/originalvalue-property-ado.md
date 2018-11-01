---
title: OriginalValue プロパティ (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 872e7c88e5ea4e79d6bff4aa590e72743feb3893
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884913"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="5cf68-102">OriginalValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cf68-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="5cf68-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5cf68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cf68-104">変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。</span><span class="sxs-lookup"><span data-stu-id="5cf68-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cf68-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="5cf68-105">Return value</span></span>

<span data-ttu-id="5cf68-106">変更前のフィールドの値を表すバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="5cf68-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf68-107">解説</span><span class="sxs-lookup"><span data-stu-id="5cf68-107">Remarks</span></span>

<span data-ttu-id="5cf68-108">現在のレコードからフィールドの元の値を返すには、 **OriginalValue** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cf68-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="5cf68-109">*イミディ エイト更新モード*(でプロバイダーに変更を書き込みます、基になるデータ ソース[の更新](update-method-ado.md)メソッドを呼び出した後)、 **OriginalValue**プロパティは、変更する前に存在していたフィールドの値を返します (以後、最後の**Update**メソッドの呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="5cf68-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="5cf68-110">これは、 [Value](value-property-ado.md)プロパティを置換するのには、 [CancelUpdate](cancelupdate-method-ado.md)メソッドを使用するのと同じ値です。</span><span class="sxs-lookup"><span data-stu-id="5cf68-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="5cf68-111">*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **OriginalValue**プロパティは、いずれかの前に存在していたフィールドの値を返します(つまり、最後の**UpdateBatch**メソッドを呼び出す) ために変更します。</span><span class="sxs-lookup"><span data-stu-id="5cf68-111">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="5cf68-112">これは、 **Value**プロパティを置換するのには、 [CancelBatch](cancelbatch-method-ado.md)メソッドを使用するのと同じ値です。</span><span class="sxs-lookup"><span data-stu-id="5cf68-112">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="5cf68-113">[UnderlyingValue](underlyingvalue-property-ado.md)プロパティを使用してこのプロパティを使用する場合は、バッチ更新で発生した競合を解決できます。</span><span class="sxs-lookup"><span data-stu-id="5cf68-113">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="5cf68-114">Record</span><span class="sxs-lookup"><span data-stu-id="5cf68-114">Record</span></span>

<span data-ttu-id="5cf68-115">[Record](record-object-ado.md) オブジェクトの場合、 **Update** を呼び出す前に追加されたフィールドの [OriginalValue](update-method-ado.md) プロパティは空になります。</span><span class="sxs-lookup"><span data-stu-id="5cf68-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

