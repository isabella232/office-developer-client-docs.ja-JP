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
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428691"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="bf277-103">Transport-Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="bf277-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="bf277-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf277-105">TNEF は、一連の MAPI プロパティ (MAPI メッセージ) を連続したデータ ストリームに変換するための形式です。</span><span class="sxs-lookup"><span data-stu-id="bf277-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="bf277-106">TNEF 関数は、主に、これらのプロパティを直接サポートしないメッセージング システムを介して送信するために MAPI メッセージ プロパティをエンコードする必要があるトランスポート プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf277-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="bf277-107">たとえば、SMTP ベースのトランスポートは TNEF を使用して **、SMTP** メッセージの構造に直接表現されていない PR_SENT_REPRESENTING_NAME ([PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)などのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="bf277-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="bf277-108">TNEF 実装では、複数の TNEF 固有の属性を定義します。それぞれの属性は、特定の MAPI プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="bf277-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="bf277-109">これらの属性は、それぞれの MAPI プロパティを TNEF ストリームにエンコードするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf277-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="bf277-110">さらに、特定の属性が対応していない MAPI プロパティをカプセル化するために使用できる特別な属性が定義されています。</span><span class="sxs-lookup"><span data-stu-id="bf277-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="bf277-111">これらの属性が定義されている理由は、すべての MAPI プロパティに対して単に統一エンコード方式を使用する代わりに、TNEF を使用している MAPI 準拠以外のソフトウェアとの下位互換性を有効にしている理由です。</span><span class="sxs-lookup"><span data-stu-id="bf277-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="bf277-112">このセクションの残りの部分では、TNEF ストリームの構造と構文、MAPI プロパティと TNEF 属性間のマッピング、および特定の TNEF 属性に関する重要な考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf277-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

