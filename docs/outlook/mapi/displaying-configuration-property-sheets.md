---
title: 構成プロパティ シートの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421313"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="38745-103">構成プロパティ シートの表示</span><span class="sxs-lookup"><span data-stu-id="38745-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="38745-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38745-105">トランスポート プロバイダーは [、IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) メソッドを使用して構成プロパティ シートを実装します。</span><span class="sxs-lookup"><span data-stu-id="38745-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="38745-106">**DoConfigPropSheet を呼** び出す場合、トランスポート プロバイダーはプロパティの配列へのポインターと、プロパティの表示方法に関する情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="38745-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="38745-107">MAPI は、標準のダイアログ ボックスを使用してユーザーにプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="38745-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="38745-108">一貫性のあるインターフェイスをユーザーに提供する利点のために、トランスポート プロバイダーを実装する場合は、このプロパティ シートメカニズムを使用してください。</span><span class="sxs-lookup"><span data-stu-id="38745-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="38745-109">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="38745-109">Transport providers</span></span>

<span data-ttu-id="38745-110">トランスポート プロバイダーは [、BuildDisplayTable](builddisplaytable.md) 関数を使用して **、DoConfigPropSheet** で使用する表示テーブルの構築を簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="38745-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="38745-111">トランスポート プロバイダーは、プロパティ シート API を直接使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="38745-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="38745-112">プロパティの変更をバッファー処理するために、トランスポート プロバイダーは [CreateIProp 関数を使用](createiprop.md) できます。</span><span class="sxs-lookup"><span data-stu-id="38745-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="38745-113">これにより、ユーザーがプロパティに格納されている値を変更する間、ユーザーによる取り消しの処理が簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="38745-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="38745-114">必要に応じて、トランスポート プロバイダーは、ユーザーの構成タスクを簡略化するためのウィザード ダイアログ ボックスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="38745-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

