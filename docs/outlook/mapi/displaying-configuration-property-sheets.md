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
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588357"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="a027d-103">構成のプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="a027d-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="a027d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a027d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a027d-105">トランスポート プロバイダーは、プロパティ シートの構成を実装するために[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a027d-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="a027d-106">**DoConfigPropSheet**を呼び出すと、トランスポート プロバイダーはそれらを表示する方法についての情報とプロパティの配列をポインターで渡します。</span><span class="sxs-lookup"><span data-stu-id="a027d-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="a027d-107">MAPI ではユーザーにプロパティが、標準のダイアログ ボックスを使用してに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a027d-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="a027d-108">一貫性のあるインターフェイスのユーザーにとってのメリットのためのトランスポート プロバイダーを実装する場合、このプロパティ シートのメカニズムを使用するよう強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a027d-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="a027d-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a027d-109">Transport providers</span></span>

<span data-ttu-id="a027d-110">トランスポート プロバイダーは、 **DoConfigPropSheet**で使用するため、表示された表の作成を簡略化するのに[BuildDisplayTable](builddisplaytable.md)関数を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a027d-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="a027d-111">トランスポート プロバイダーは、プロパティ シート API を直接使用することができますもします。</span><span class="sxs-lookup"><span data-stu-id="a027d-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="a027d-112">バッファーのプロパティを変更するには、トランスポート プロバイダーは、 [CreateIProp](createiprop.md)関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a027d-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="a027d-113">ユーザー プロパティに格納されている値を変更するときに、ユーザーがキャンセルの処理が簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="a027d-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="a027d-114">かどうか、必要に応じてトランスポート プロバイダーも提供できますウィザード ダイアログ ボックスがユーザーの構成作業を簡略化します。</span><span class="sxs-lookup"><span data-stu-id="a027d-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

