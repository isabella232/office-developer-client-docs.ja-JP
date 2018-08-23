---
title: マッピングとマッピングの署名
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b5c8fd8c757de995e2a2e4239be614cf171fcb44
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566188"
---
# <a name="mappings-and-mapping-signatures"></a><span data-ttu-id="c7fcf-103">マッピングとマッピングの署名</span><span class="sxs-lookup"><span data-stu-id="c7fcf-103">Mappings and Mapping Signatures</span></span>

  
  
<span data-ttu-id="c7fcf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7fcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7fcf-105">サービス プロバイダーは、名前付きプロパティをサポートする場合、id と名前のペアの各セットをマッピングと呼びます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-105">When a service provider supports named properties, each set of identifier and name pairs is referred to as a mapping.</span></span> <span data-ttu-id="c7fcf-106">マッピングの 1 つまたは複数のサービス プロバイダーをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-106">Service providers can support one mapping or several.</span></span> <span data-ttu-id="c7fcf-107">1 つのメッセージ ストア プロバイダー、たとえば、すべてのメッセージ、フォルダー、およびメッセージ ストアのオブジェクト名と、対応する識別子の 1 つのリストを操作するのに**GetIDsFromNames**および**GetNamesFromIDs**メソッドを実装できます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-107">That is, one message store provider, for example, can implement the **GetIDsFromNames** and **GetNamesFromIDs** methods for all of its message, folder, and message store objects to work with a single list of names and their corresponding identifiers.</span></span> <span data-ttu-id="c7fcf-108">別のメッセージ ストア プロバイダーは、すべてのフォルダーと、それに含まれるメッセージの 1 つのリストまたはすべてのメッセージとすべてのフォルダーの一意のリストを実装可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-108">Another message store provider might have one list for every folder and the messages contained within it, or implement a unique list for every message and every folder.</span></span> <span data-ttu-id="c7fcf-109">メッセージごとに固有のマッピングを使用するメッセージ ストア プロバイダーは、指定したプロパティ名のプロパティの識別子がメッセージからを異なるため、フォルダーの内容のテーブルに表示する名前付きプロパティを許可できません。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-109">Message store providers that use a unique mapping for every message must not allow named properties to appear in their folder contents tables because for a given property name, the property identifier will differ from message to message.</span></span> <span data-ttu-id="c7fcf-110">MAPI では、プロバイダーがシンプルにして、すべてのテーブルを含むオブジェクトの 1 つのリストで、操作をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-110">MAPI recommends that providers keep it simple and operate with a single list for all of their objects including tables.</span></span> 
  
<span data-ttu-id="c7fcf-111">すべてのマッピングでは、サービス ・ プロバイダーにマッピング署名ことが必要です。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-111">For every mapping, service providers must supply a mapping signature.</span></span> <span data-ttu-id="c7fcf-112">マッピングの署名とは、通常、GUID、一連のプロパティ識別子と、対応する名前を一意に識別するバイナリ値です。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-112">A mapping signature is a binary value, usually a GUID, that uniquely identifies a set of property identifiers and their corresponding names.</span></span> <span data-ttu-id="c7fcf-113">署名のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) に格納されます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-113">Mapping signatures are stored in an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="c7fcf-114">サービス プロバイダーは、それが表すマップに変更が加えられるたびに、 **PR_MAPPING_SIGNATURE**プロパティの値を変更しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-114">Service providers must change the value for their **PR_MAPPING_SIGNATURE** property whenever a change is made to the mapping that it represents.</span></span> <span data-ttu-id="c7fcf-115">たとえば、名前または新しい名前に新しい識別子が割り当てられている識別子のペアが追加された場合は、 **PR_MAPPING_SIGNATURE**を更新しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-115">For example, **PR_MAPPING_SIGNATURE** must be updated if a new identifier is assigned to a name or a new name and identifier pair is added.</span></span> 
  
<span data-ttu-id="c7fcf-116">オブジェクトの名前付きプロパティを操作するクライアントでは、比較、およびコピーの操作でオブジェクトの**PR_MAPPING_SIGNATURE**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-116">Clients working with the named properties of objects use the objects' **PR_MAPPING_SIGNATURE** properties in comparison and copy operations.</span></span> <span data-ttu-id="c7fcf-117">比較するには、プロパティの識別子の 2 つのオブジェクトに属する、マッピングの署名を使用しないクライアント呼び出す必要があります[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)の両方のオブジェクトの識別子の名前を取得するという名前です。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-117">To compare named property identifiers belonging to two objects, clients not using mapping signatures must call [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) on both objects to retrieve the names for each of the identifiers.</span></span> <span data-ttu-id="c7fcf-118">オブジェクトのマッピングの署名を使用すると、この呼び出しが不要なレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-118">Using the mapping signatures of objects can render this call unnecessary.</span></span> <span data-ttu-id="c7fcf-119">2 つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値が同じ場合、同じマッピングを使用します。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-119">When two objects have the same value for their **PR_MAPPING_SIGNATURE** properties, they use the same mapping.</span></span> <span data-ttu-id="c7fcf-120">同じマッピングを使用する識別子を直接比較することができます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-120">Identifiers that use the same mapping can be compared directly.</span></span> <span data-ttu-id="c7fcf-121">[IMAPIProp::CopyTo](imapiprop-copyto.md)と[IMAPIProp::CopyProps](imapiprop-copyprops.md)を実装するサービス プロバイダーでは、オブジェクトのマッピングの署名のも利用できます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-121">Service providers that implement [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) can also take advantage of an object's mapping signature.</span></span> <span data-ttu-id="c7fcf-122">コピーという名前のオブジェクトのプロパティと、サービス プロバイダーは、元とコピー先のオブジェクトが同じマッピング シグネチャを持つ場合の変換手順を回避できます。</span><span class="sxs-lookup"><span data-stu-id="c7fcf-122">When copying named properties between objects, service providers can avoid the conversion step when the source and destination objects have the same mapping signature.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7fcf-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7fcf-123">See also</span></span>



[<span data-ttu-id="c7fcf-124">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7fcf-124">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="c7fcf-125">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="c7fcf-125">MAPI Named Properties</span></span>](mapi-named-properties.md)

