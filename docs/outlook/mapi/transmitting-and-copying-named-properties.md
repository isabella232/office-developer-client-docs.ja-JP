---
title: 名前付きプロパティの送信とコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437778"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="79c79-103">名前付きプロパティの送信とコピー</span><span class="sxs-lookup"><span data-stu-id="79c79-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="79c79-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79c79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79c79-105">名前付きプロパティの送信、移動、またはコピーの場合、名前は変更されませんが、識別子は、目的のオブジェクトのマッピングに準拠するように変更される必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c79-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="79c79-106">このルールの唯一の例外は、移行元と移行先が同じマッピング署名を持っており、再マッピングが不要な場合です。</span><span class="sxs-lookup"><span data-stu-id="79c79-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="79c79-107">転送される名前付きプロパティの名前を、送信先で動作する適切な識別子に再マップするのは、トランスポートプロバイダーの役割です。</span><span class="sxs-lookup"><span data-stu-id="79c79-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="79c79-108">送信側のトランスポートプロバイダーは、宛先に正しいマッピングがあるかどうかを知ることができません。名前を送信し、受信側トランスポートプロバイダーによって、それが動作する識別子にマップされるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c79-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="79c79-109">MAPI 実装の TNEF は、トランスポートプロバイダーの名前付きプロパティのマッピングを処理します。</span><span class="sxs-lookup"><span data-stu-id="79c79-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="79c79-110">トランスポートプロバイダーは、手動で再マッピングを処理するか、TNEF 実装を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="79c79-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="79c79-111">これらのプロパティをメッセージストア間でコピーするときに、名前付きプロパティの同様の再マッピングが発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c79-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="79c79-112">ただし、メッセージストアプロバイダーは、送信先の識別子マッピングの名前を取得できるため、すぐにプロパティをマップし直すことができ、宛先のメッセージストアに依存する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="79c79-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79c79-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="79c79-113">See also</span></span>



[<span data-ttu-id="79c79-114">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="79c79-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

