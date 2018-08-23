---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: SMTP アカウントに使用する暗号化された接続の種類を指定します。
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799579"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="9b966-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="9b966-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="9b966-104">SMTP アカウントに使用する暗号化された接続の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="9b966-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9b966-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9b966-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b966-106">識別子:</span><span class="sxs-lookup"><span data-stu-id="9b966-106">Identifier:</span></span>  <br/> |<span data-ttu-id="9b966-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="9b966-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="9b966-108">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="9b966-108">Property type:</span></span>  <br/> |<span data-ttu-id="9b966-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="9b966-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="9b966-110">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="9b966-110">Property tag:</span></span>  <br/> |<span data-ttu-id="9b966-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="9b966-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="9b966-112">アクセス:</span><span class="sxs-lookup"><span data-stu-id="9b966-112">Access:</span></span>  <br/> |<span data-ttu-id="9b966-113">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9b966-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b966-114">注釈</span><span class="sxs-lookup"><span data-stu-id="9b966-114">Remarks</span></span>

<span data-ttu-id="9b966-115">値には、以下の定数のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9b966-115">The value can be one of the following constants.</span></span> <span data-ttu-id="9b966-116">その値の[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b966-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="9b966-117">**定数**</span><span class="sxs-lookup"><span data-stu-id="9b966-117">**Constants**</span></span>|<span data-ttu-id="9b966-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="9b966-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b966-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="9b966-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="9b966-120">暗号化を使用しません。</span><span class="sxs-lookup"><span data-stu-id="9b966-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="9b966-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="9b966-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="9b966-122">セキュア ソケット レイヤー (SSL) 暗号化を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b966-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="9b966-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="9b966-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="9b966-124">トランスポート層セキュリティ (TLS) の暗号化および認証プロトコルを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b966-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="9b966-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="9b966-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="9b966-126">自動的に検出し、メール サーバーでサポートされている暗号化方式を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b966-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b966-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b966-127">See also</span></span>

- [<span data-ttu-id="9b966-128">POP3 アカウントのメッセージ ダウンロードの管理</span><span class="sxs-lookup"><span data-stu-id="9b966-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="9b966-129">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="9b966-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

