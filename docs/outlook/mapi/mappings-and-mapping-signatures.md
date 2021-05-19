---
title: マッピングとマッピングの署名
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410015"
---
# <a name="mappings-and-mapping-signatures"></a><span data-ttu-id="cc906-103">マッピングとマッピングの署名</span><span class="sxs-lookup"><span data-stu-id="cc906-103">Mappings and Mapping Signatures</span></span>

  
  
<span data-ttu-id="cc906-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc906-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc906-105">サービス プロバイダーが名前付きプロパティをサポートしている場合、識別子と名前のペアの各セットはマッピングと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cc906-105">When a service provider supports named properties, each set of identifier and name pairs is referred to as a mapping.</span></span> <span data-ttu-id="cc906-106">サービス プロバイダーは、1 つのマッピングまたは複数のマッピングをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="cc906-106">Service providers can support one mapping or several.</span></span> <span data-ttu-id="cc906-107">つまり、たとえば、1 つのメッセージ ストア プロバイダーは、すべてのメッセージ、フォルダー、およびメッセージ ストア オブジェクトに対して **GetIDsFromNames** メソッドと **GetNamesFromIDs** メソッドを実装して、名前と対応する識別子の 1 つのリストを操作できます。</span><span class="sxs-lookup"><span data-stu-id="cc906-107">That is, one message store provider, for example, can implement the **GetIDsFromNames** and **GetNamesFromIDs** methods for all of its message, folder, and message store objects to work with a single list of names and their corresponding identifiers.</span></span> <span data-ttu-id="cc906-108">別のメッセージ ストア プロバイダーは、フォルダーごとに 1 つのリストを持ち、その中に含まれるメッセージを持つ場合や、すべてのメッセージとフォルダーごとに一意のリストを実装する場合があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-108">Another message store provider might have one list for every folder and the messages contained within it, or implement a unique list for every message and every folder.</span></span> <span data-ttu-id="cc906-109">すべてのメッセージに対して一意のマッピングを使用するメッセージ ストア プロバイダーは、指定されたプロパティ名に対して、プロパティ識別子がメッセージごとに異なるので、フォルダーコンテンツ テーブルに名前付きプロパティを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="cc906-109">Message store providers that use a unique mapping for every message must not allow named properties to appear in their folder contents tables because for a given property name, the property identifier will differ from message to message.</span></span> <span data-ttu-id="cc906-110">MAPI では、プロバイダーが単純な状態を維持し、テーブルを含むすべてのオブジェクトに対して 1 つのリストで操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-110">MAPI recommends that providers keep it simple and operate with a single list for all of their objects including tables.</span></span> 
  
<span data-ttu-id="cc906-111">マッピングごとに、サービス プロバイダーはマッピング署名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-111">For every mapping, service providers must supply a mapping signature.</span></span> <span data-ttu-id="cc906-112">マッピング署名は、一連のプロパティ識別子と対応する名前を一意に識別するバイナリ値 (通常は GUID) です。</span><span class="sxs-lookup"><span data-stu-id="cc906-112">A mapping signature is a binary value, usually a GUID, that uniquely identifies a set of property identifiers and their corresponding names.</span></span> <span data-ttu-id="cc906-113">マッピング署名は、オブジェクトのプロパティ ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md) **)** PR_MAPPING_SIGNATUREに格納されます。</span><span class="sxs-lookup"><span data-stu-id="cc906-113">Mapping signatures are stored in an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="cc906-114">サービス プロバイダーは、それが表すマッピングに変更 **PR_MAPPING_SIGNATURE** プロパティの値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-114">Service providers must change the value for their **PR_MAPPING_SIGNATURE** property whenever a change is made to the mapping that it represents.</span></span> <span data-ttu-id="cc906-115">たとえば、新 **PR_MAPPING_SIGNATURE** が名前に割り当てられている場合、または新しい名前と識別子のペアが追加されている場合は、新しい識別子を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-115">For example, **PR_MAPPING_SIGNATURE** must be updated if a new identifier is assigned to a name or a new name and identifier pair is added.</span></span> 
  
<span data-ttu-id="cc906-116">オブジェクトの名前付きプロパティを操作するクライアントは、比較 **および** コピー操作PR_MAPPING_SIGNATUREオブジェクトのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc906-116">Clients working with the named properties of objects use the objects' **PR_MAPPING_SIGNATURE** properties in comparison and copy operations.</span></span> <span data-ttu-id="cc906-117">2 つのオブジェクトに属する名前付きプロパティ識別子を比較するには、マッピング署名を使用していないクライアントは、両方のオブジェクトで [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) を呼び出して、各識別子の名前を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc906-117">To compare named property identifiers belonging to two objects, clients not using mapping signatures must call [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) on both objects to retrieve the names for each of the identifiers.</span></span> <span data-ttu-id="cc906-118">オブジェクトのマッピング署名を使用すると、この呼び出しが不要になります。</span><span class="sxs-lookup"><span data-stu-id="cc906-118">Using the mapping signatures of objects can render this call unnecessary.</span></span> <span data-ttu-id="cc906-119">2 つのオブジェクトのプロパティの値が同 **PR_MAPPING_SIGNATURE、同** じマッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc906-119">When two objects have the same value for their **PR_MAPPING_SIGNATURE** properties, they use the same mapping.</span></span> <span data-ttu-id="cc906-120">同じマッピングを使用する識別子を直接比較できます。</span><span class="sxs-lookup"><span data-stu-id="cc906-120">Identifiers that use the same mapping can be compared directly.</span></span> <span data-ttu-id="cc906-121">[IMAPIProp::CopyTo](imapiprop-copyto.md)と[IMAPIProp::CopyProps](imapiprop-copyprops.md)を実装するサービス プロバイダーは、オブジェクトのマッピング署名を利用できます。</span><span class="sxs-lookup"><span data-stu-id="cc906-121">Service providers that implement [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) can also take advantage of an object's mapping signature.</span></span> <span data-ttu-id="cc906-122">名前付きプロパティをオブジェクト間でコピーする場合、サービス プロバイダーは、ソース オブジェクトと変換先オブジェクトが同じマッピング署名を持つ場合、変換手順を回避できます。</span><span class="sxs-lookup"><span data-stu-id="cc906-122">When copying named properties between objects, service providers can avoid the conversion step when the source and destination objects have the same mapping signature.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc906-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc906-123">See also</span></span>



[<span data-ttu-id="cc906-124">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc906-124">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="cc906-125">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="cc906-125">MAPI Named Properties</span></span>](mapi-named-properties.md)

