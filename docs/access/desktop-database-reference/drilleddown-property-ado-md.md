---
title: DrilledDown プロパティ (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96edfa035937a201891f0dca2aeaf036a5061cfe
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605493"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="39095-102">DrilledDown プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="39095-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="39095-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="39095-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="39095-104">軸上でメンバーの直下に子がないかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="39095-104">Indicates whether no children immediately follow the member on the axis.</span></span>

<span data-ttu-id="39095-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="39095-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="39095-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="39095-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="39095-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="39095-107">Return values</span></span>
>>>>>>> <span data-ttu-id="39095-108">master</span><span class="sxs-lookup"><span data-stu-id="39095-108">master</span></span>

<span data-ttu-id="39095-p101">ブール型 ( **Boolean** ) の値を取得します。値の取得のみが可能です。 **DrilledDown** プロパティは、軸上の現在のメンバーに子メンバーがない場合、 **True** を返します。軸上の現在のメンバーに 1 つ以上の子メンバーがある場合、 **DrilledDown** プロパティは **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="39095-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="39095-112">解説</span><span class="sxs-lookup"><span data-stu-id="39095-112">Remarks</span></span>

<span data-ttu-id="39095-p102">**DrilledDown** プロパティを使用すると、軸上の現在のメンバーの直下に少なくとも 1 つの子があるかどうかを調べることができます。この情報は、メンバーを表示する際に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="39095-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="39095-p103">このプロパティは、[Position](member-object-ado-md.md) オブジェクトに属している [Member](position-object-ado-md.md) オブジェクトのみでサポートされています。 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="39095-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

