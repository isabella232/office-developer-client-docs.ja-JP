---
title: メッセージ ストア プロバイダーの構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415888"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="254b8-103">メッセージ ストア プロバイダーの構成インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="254b8-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="254b8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="254b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="254b8-105">メッセージ ストア プロバイダーは、ユーザーがメッセージ ストア プロバイダーを構成してそのユーザーのコンピューターで実行できるインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="254b8-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="254b8-106">通常、メッセージ ストア プロバイダーは、メッセージ ストア プロバイダーがユーザーのプロファイルに追加される場合に構成されます。</span><span class="sxs-lookup"><span data-stu-id="254b8-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="254b8-107">メッセージ ストア プロバイダーの構成インターフェイスは、通常、保護されたメッセージ ストアのユーザー名とパスワードの設定、必要なファイルへのパスの選択、必要に応じて使用する基になるストレージ メカニズムの作成などのタスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="254b8-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="254b8-108">実装する構成インターフェイスには、メッセージ サービス プロバイダーの DLL 内の追加のエントリ ポイントからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="254b8-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="254b8-109">詳細については、「メッセージ サービス [の構成」を参照してください](configuring-a-message-service.md)。</span><span class="sxs-lookup"><span data-stu-id="254b8-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="254b8-110">メッセージ ストア プロバイダーの構成インターフェイスは、メッセージ ストア プロバイダーが実装する必要がある唯一のユーザー インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="254b8-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="254b8-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="254b8-111">See also</span></span>



<span data-ttu-id="254b8-112">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="254b8-112">[Message Store Features](message-store-features.md)</span></span>

