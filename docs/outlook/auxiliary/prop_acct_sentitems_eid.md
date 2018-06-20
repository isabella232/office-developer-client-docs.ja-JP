---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799559"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="3f3ee-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="3f3ee-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="3f3ee-104">アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3f3ee-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3f3ee-105">Quick info</span></span>

<span data-ttu-id="3f3ee-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f3ee-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="3f3ee-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3f3ee-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="3f3ee-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="3f3ee-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3f3ee-109">Property type:</span></span>  <br/> |<span data-ttu-id="3f3ee-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3f3ee-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3f3ee-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3f3ee-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="3f3ee-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="3f3ee-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="3f3ee-113">Access:</span></span>  <br/> |<span data-ttu-id="3f3ee-114">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f3ee-115">備考</span><span class="sxs-lookup"><span data-stu-id="3f3ee-115">Remarks</span></span>

<span data-ttu-id="3f3ee-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="3f3ee-117">送信済みアイテムの既定のフォルダーは、**送信済みアイテム**です。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="3f3ee-118">このプロパティは、POP3 および IMAP アカウントの読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="3f3ee-119">これらの種類のアカウントに対してこのプロパティを設定すると、 **E_ACCT_NOT_FOUND**が返されます。</span><span class="sxs-lookup"><span data-stu-id="3f3ee-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

