---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327588"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="15727-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="15727-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="15727-104">アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。</span><span class="sxs-lookup"><span data-stu-id="15727-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="15727-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="15727-105">Quick info</span></span>

<span data-ttu-id="15727-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15727-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15727-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="15727-107">Identifier:</span></span>  <br/> |<span data-ttu-id="15727-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="15727-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="15727-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="15727-109">Property type:</span></span>  <br/> |<span data-ttu-id="15727-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="15727-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="15727-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="15727-111">Property tag:</span></span>  <br/> |<span data-ttu-id="15727-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="15727-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="15727-113">接続</span><span class="sxs-lookup"><span data-stu-id="15727-113">Access:</span></span>  <br/> |<span data-ttu-id="15727-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="15727-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15727-115">解説</span><span class="sxs-lookup"><span data-stu-id="15727-115">Remarks</span></span>

<span data-ttu-id="15727-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="15727-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="15727-117">送信済みアイテムの既定のフォルダーは、[**送信済みアイテム**] です。</span><span class="sxs-lookup"><span data-stu-id="15727-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="15727-118">このプロパティは、POP3 および IMAP のアカウントでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="15727-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="15727-119">これらの種類のアカウントに対してこのプロパティを設定しようとすると、 **E_ACCT_NOT_FOUND**が返されます。</span><span class="sxs-lookup"><span data-stu-id="15727-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

