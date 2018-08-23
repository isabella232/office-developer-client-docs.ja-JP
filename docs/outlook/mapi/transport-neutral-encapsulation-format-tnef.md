---
title: Transport-Neutral Encapsulation Format (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 440c27b019b91ec8c2c02e37850d2768a273559b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591934"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="9d94b-103">Transport-Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="9d94b-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="9d94b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d94b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d94b-105">TNEF は、MAPI プロパティのセットを変換するための形式: MAPI メッセージ-シリアル データ ストリームにします。</span><span class="sxs-lookup"><span data-stu-id="9d94b-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="9d94b-106">TNEF 関数は、これらのプロパティを直接サポートしていないメッセージング システムを通じて送信するための MAPI メッセージのプロパティをエンコードするために必要とするトランスポート プロバイダーによって主に使用します。</span><span class="sxs-lookup"><span data-stu-id="9d94b-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="9d94b-107">など、SMTP ベースのトランスポートでは、SMTP メッセージの構造体に直接表現されていない**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) などのプロパティをエンコードするために TNEF を使用します。</span><span class="sxs-lookup"><span data-stu-id="9d94b-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="9d94b-108">TNEF の実装では、特定の MAPI プロパティに対応する、いくつかの TNEF 固有の属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="9d94b-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="9d94b-109">TNEF ストリームに、それぞれの MAPI プロパティをエンコードするためには、これらの属性が使用されます。</span><span class="sxs-lookup"><span data-stu-id="9d94b-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="9d94b-110">特殊な属性を定義するさらに、それに対応する特定の属性を持たない任意の MAPI プロパティをカプセル化するのにを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9d94b-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="9d94b-111">これらの属性が定義されている理由: 統一されたすべての MAPI プロパティのエンコードを使用するだけではなく、TNEF を使用している MAPI 準拠のソフトウェアとの下位互換性を有効にするのには。</span><span class="sxs-lookup"><span data-stu-id="9d94b-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="9d94b-112">このセクションの残りの部分では、TNEF ストリームでは、MAPI プロパティと TNEF 属性では、TNEF の特定の属性の重要な考慮事項とのマッピングの構文、構造体について説明します。</span><span class="sxs-lookup"><span data-stu-id="9d94b-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

