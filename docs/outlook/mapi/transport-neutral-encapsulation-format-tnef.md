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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356631"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="5362c-103">Transport-Neutral Encapsulation Format (TNEF)</span><span class="sxs-lookup"><span data-stu-id="5362c-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="5362c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5362c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5362c-105">TNEF は、一連の MAPI プロパティ (MAPI メッセージ) を連続したデータ ストリームに変換するための形式です。</span><span class="sxs-lookup"><span data-stu-id="5362c-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="5362c-106">TNEF 関数は、主に、これらのプロパティを直接サポートしていないメッセージングシステムを経由して送信するために MAPI メッセージプロパティをエンコードする必要があるトランスポートプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="5362c-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="5362c-107">たとえば、smtp ベースのトランスポートは TNEF を使用して、 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) などのプロパティをエンコードします。これは、smtp メッセージの構造に直接表現されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="5362c-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="5362c-108">tnef 実装では、いくつかの tnef 固有の属性が定義されています。これらはそれぞれ特定の MAPI プロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="5362c-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="5362c-109">これらの属性は、それぞれの MAPI プロパティを TNEF ストリームにエンコードするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5362c-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="5362c-110">さらに、特定の属性を持たない MAPI プロパティをカプセル化するために使用できる特別な属性が定義されています。</span><span class="sxs-lookup"><span data-stu-id="5362c-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="5362c-111">これらの属性が定義されている理由は、すべての mapi プロパティに対して均一なエンコード方法を使用するのではなく、TNEF を使用している mapi に準拠していないソフトウェアとの下位互換性を有効にすることです。</span><span class="sxs-lookup"><span data-stu-id="5362c-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="5362c-112">このセクションの残りの部分では、tnef ストリームの構造と構文、MAPI プロパティと TNEF 属性間のマッピング、および特定の TNEF 属性に関する重要な考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="5362c-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  

