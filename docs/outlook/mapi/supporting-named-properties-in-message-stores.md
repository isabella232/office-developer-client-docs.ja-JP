---
title: ���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b1aa0228cdc8cf6f0b2bb321e62e40127775a6de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804043"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="08b0d-103">���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="08b0d-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="08b0d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08b0d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08b0d-105">メッセージ オブジェクトは、MAPI によって定義されたプロパティのセットに含まれないことでプロパティを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="08b0d-105">Message objects can have properties in them that are not in the set of properties defined by MAPI.</span></span> <span data-ttu-id="08b0d-106">などのプロパティの名前または名前付きことができます。</span><span class="sxs-lookup"><span data-stu-id="08b0d-106">Such properties can be unnamed or named.</span></span> <span data-ttu-id="08b0d-107">名前のないプロパティは、MAPI によって定義されているプロパティの識別子の範囲内になければなりません。</span><span class="sxs-lookup"><span data-stu-id="08b0d-107">Unnamed properties must reside in a range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="08b0d-108">名前付きカスタム プロパティは、MAPI によって定義されているプロパティの識別子の別の範囲に存在します。</span><span class="sxs-lookup"><span data-stu-id="08b0d-108">Named custom properties reside in a different range of property identifiers defined by MAPI.</span></span> <span data-ttu-id="08b0d-109">カスタム メッセージの種類によって通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="08b0d-109">They are typically used by custom message types.</span></span> <span data-ttu-id="08b0d-110">メッセージ ストア プロバイダーは、既定のメッセージ ストアとして使用する場合は、名前付きプロパティをサポートしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="08b0d-110">Your message store provider must support named properties if it is to be used as the default message store.</span></span> <span data-ttu-id="08b0d-111">名前付きプロパティのサポートは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)と[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)のメソッドを実装して、どのような名前を識別する 1 つまたは複数のマッピングの署名を実装することがどのようなプロパティの識別子を持つ移動を意味します。</span><span class="sxs-lookup"><span data-stu-id="08b0d-111">Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers.</span></span> <span data-ttu-id="08b0d-112">詳細については、[新しい MAPI プロパティを定義する](defining-new-mapi-properties.md)、[名前付きプロパティのサポート](supporting-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08b0d-112">For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="08b0d-113">ほとんどのメッセージは、名前付きプロパティ マッピングの 1 つの署名、メッセージ ・ ストア内のすべてのオブジェクトをサポートするプロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="08b0d-113">Most message store providers that support named properties use a single mapping signature for all objects in the message store.</span></span> <span data-ttu-id="08b0d-114">2 つの利点があります。</span><span class="sxs-lookup"><span data-stu-id="08b0d-114">This has two benefits.</span></span> <span data-ttu-id="08b0d-115">まず、追跡するために 1 つだけを使用する必要がある場合、マッピングの署名を実装する方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="08b0d-115">First, it is simpler to implement mapping signatures if there is only one to keep track of.</span></span> <span data-ttu-id="08b0d-116">第 2 に、メッセージ ・ ストア内のすべてのオブジェクトは、同じマッピング シグネチャを使用している場合クライアント アプリケーションは確実にメッセージ ・ ストア内のメッセージのすべてのプロパティの識別子が同じ名前付きプロパティを実際に参照することです。</span><span class="sxs-lookup"><span data-stu-id="08b0d-116">Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property.</span></span> <span data-ttu-id="08b0d-117">これにより、クライアント アプリケーションのフォルダー ビューのインターフェイスの名前付きプロパティの列を表示します。</span><span class="sxs-lookup"><span data-stu-id="08b0d-117">This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08b0d-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="08b0d-118">See also</span></span>



<span data-ttu-id="08b0d-119">[���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B](implementing-messages-in-message-stores.md)</span><span class="sxs-lookup"><span data-stu-id="08b0d-119">[Implementing Messages in Message Stores](implementing-messages-in-message-stores.md)</span></span>

