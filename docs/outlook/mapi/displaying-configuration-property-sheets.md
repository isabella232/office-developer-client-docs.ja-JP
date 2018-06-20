---
title: 構成のプロパティ シートを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aa3ddecbd5af56eef16f5ae3a349a027e689fc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799939"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="e4a52-103">構成のプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="e4a52-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="e4a52-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4a52-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4a52-105">トランスポート プロバイダーは、プロパティ シートの構成を実装するために[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4a52-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="e4a52-106">**DoConfigPropSheet**を呼び出すと、トランスポート プロバイダーはそれらを表示する方法についての情報とプロパティの配列をポインターで渡します。</span><span class="sxs-lookup"><span data-stu-id="e4a52-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="e4a52-107">MAPI ではユーザーにプロパティが、標準のダイアログ ボックスを使用してに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4a52-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="e4a52-108">一貫性のあるインターフェイスのユーザーにとってのメリットのためのトランスポート プロバイダーを実装する場合、このプロパティ シートのメカニズムを使用するよう強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e4a52-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="e4a52-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e4a52-109">Transport providers</span></span>

<span data-ttu-id="e4a52-110">トランスポート プロバイダーは、 **DoConfigPropSheet**で使用するため、表示された表の作成を簡略化するのに[BuildDisplayTable](builddisplaytable.md)関数を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e4a52-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="e4a52-111">トランスポート プロバイダーは、プロパティ シート API を直接使用することができますもします。</span><span class="sxs-lookup"><span data-stu-id="e4a52-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="e4a52-112">バッファーのプロパティを変更するには、トランスポート プロバイダーは、 [CreateIProp](createiprop.md)関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4a52-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="e4a52-113">ユーザー プロパティに格納されている値を変更するときに、ユーザーがキャンセルの処理が簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="e4a52-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="e4a52-114">かどうか、必要に応じてトランスポート プロバイダーも提供できますウィザード ダイアログ ボックスがユーザーの構成作業を簡略化します。</span><span class="sxs-lookup"><span data-stu-id="e4a52-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

