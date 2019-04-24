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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357639"
---
# <a name="mappings-and-mapping-signatures"></a><span data-ttu-id="c446e-103">マッピングとマッピングの署名</span><span class="sxs-lookup"><span data-stu-id="c446e-103">Mappings and Mapping Signatures</span></span>

  
  
<span data-ttu-id="c446e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c446e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c446e-105">サービスプロバイダーが名前付きプロパティをサポートしている場合、識別子と名前のペアの各セットは、マッピングと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c446e-105">When a service provider supports named properties, each set of identifier and name pairs is referred to as a mapping.</span></span> <span data-ttu-id="c446e-106">サービスプロバイダーは、1つまたは複数のマッピングをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="c446e-106">Service providers can support one mapping or several.</span></span> <span data-ttu-id="c446e-107">たとえば、1つのメッセージストアプロバイダーでは、すべてのメッセージ、フォルダー、およびメッセージストアオブジェクトの**getidsfromnames**および**GetNamesFromIDs**メソッドを実装して、名前とそれに対応する識別子のリストを1つのリストで操作できます。</span><span class="sxs-lookup"><span data-stu-id="c446e-107">That is, one message store provider, for example, can implement the **GetIDsFromNames** and **GetNamesFromIDs** methods for all of its message, folder, and message store objects to work with a single list of names and their corresponding identifiers.</span></span> <span data-ttu-id="c446e-108">別のメッセージストアプロバイダーは、フォルダーとその中に含まれるメッセージごとに1つのリストを持つことができます。または、すべてのメッセージとすべてのフォルダーに固有のリストを実装します。</span><span class="sxs-lookup"><span data-stu-id="c446e-108">Another message store provider might have one list for every folder and the messages contained within it, or implement a unique list for every message and every folder.</span></span> <span data-ttu-id="c446e-109">メッセージストアプロバイダーは、特定のプロパティ名に関して、すべてのメッセージに一意のマッピングを使用して、名前付きプロパティをフォルダーコンテンツテーブルに表示しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c446e-109">Message store providers that use a unique mapping for every message must not allow named properties to appear in their folder contents tables because for a given property name, the property identifier will differ from message to message.</span></span> <span data-ttu-id="c446e-110">MAPI では、プロバイダーがシンプルに保持し、テーブルを含むすべてのオブジェクトに対して単一のリストを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c446e-110">MAPI recommends that providers keep it simple and operate with a single list for all of their objects including tables.</span></span> 
  
<span data-ttu-id="c446e-111">すべてのマッピングについて、サービスプロバイダーはマッピング署名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c446e-111">For every mapping, service providers must supply a mapping signature.</span></span> <span data-ttu-id="c446e-112">マッピングシグネチャはバイナリ値 (通常は GUID) で、一連のプロパティ識別子とそれに対応する名前を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="c446e-112">A mapping signature is a binary value, usually a GUID, that uniquely identifies a set of property identifiers and their corresponding names.</span></span> <span data-ttu-id="c446e-113">署名のマッピングは、オブジェクトの**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c446e-113">Mapping signatures are stored in an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="c446e-114">サービスプロバイダーが表すマッピングが変更されたときは、その**PR_MAPPING_SIGNATURE**プロパティの値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c446e-114">Service providers must change the value for their **PR_MAPPING_SIGNATURE** property whenever a change is made to the mapping that it represents.</span></span> <span data-ttu-id="c446e-115">たとえば、新しい識別子が名前または新しい名前に割り当てられ、識別子のペアが追加されている場合は、 **PR_MAPPING_SIGNATURE**を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c446e-115">For example, **PR_MAPPING_SIGNATURE** must be updated if a new identifier is assigned to a name or a new name and identifier pair is added.</span></span> 
  
<span data-ttu-id="c446e-116">オブジェクトの名前付きプロパティを操作するクライアントは、 **PR_MAPPING_SIGNATURE**プロパティを比較およびコピー操作で使用します。</span><span class="sxs-lookup"><span data-stu-id="c446e-116">Clients working with the named properties of objects use the objects' **PR_MAPPING_SIGNATURE** properties in comparison and copy operations.</span></span> <span data-ttu-id="c446e-117">2つのオブジェクトに属する名前付きプロパティ識別子を比較するには、マッピングシグネチャを使用していないクライアントは、両方のオブジェクトで[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)を呼び出して、各識別子の名前を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c446e-117">To compare named property identifiers belonging to two objects, clients not using mapping signatures must call [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) on both objects to retrieve the names for each of the identifiers.</span></span> <span data-ttu-id="c446e-118">オブジェクトのマッピングシグネチャを使用すると、この呼び出しが不要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="c446e-118">Using the mapping signatures of objects can render this call unnecessary.</span></span> <span data-ttu-id="c446e-119">2つのオブジェクトの**PR_MAPPING_SIGNATURE**プロパティの値が同じ場合は、同じマッピングを使用します。</span><span class="sxs-lookup"><span data-stu-id="c446e-119">When two objects have the same value for their **PR_MAPPING_SIGNATURE** properties, they use the same mapping.</span></span> <span data-ttu-id="c446e-120">同じマッピングを使用する識別子は、直接比較できます。</span><span class="sxs-lookup"><span data-stu-id="c446e-120">Identifiers that use the same mapping can be compared directly.</span></span> <span data-ttu-id="c446e-121">[imapiprop:: CopyTo](imapiprop-copyto.md)および[imapiprop:: copyprops](imapiprop-copyprops.md)を実装するサービスプロバイダーは、オブジェクトのマッピングシグネチャを利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="c446e-121">Service providers that implement [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) can also take advantage of an object's mapping signature.</span></span> <span data-ttu-id="c446e-122">オブジェクト間で名前付きプロパティをコピーする場合、サービスプロバイダーは、移行元とコピー先のオブジェクトが同じマッピング署名を持っている場合に、変換手順を回避できます。</span><span class="sxs-lookup"><span data-stu-id="c446e-122">When copying named properties between objects, service providers can avoid the conversion step when the source and destination objects have the same mapping signature.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c446e-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c446e-123">See also</span></span>



[<span data-ttu-id="c446e-124">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c446e-124">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="c446e-125">MAPI ���O�t���v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="c446e-125">MAPI Named Properties</span></span>](mapi-named-properties.md)

