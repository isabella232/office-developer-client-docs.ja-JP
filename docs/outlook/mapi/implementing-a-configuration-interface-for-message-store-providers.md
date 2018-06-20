---
title: メッセージ ストア プロバイダーの構成インターフェイスを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800893"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="ed2ad-103">メッセージ ストア プロバイダーの構成インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="ed2ad-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed2ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed2ad-105">メッセージ ストア プロバイダーは、そのユーザーのコンピューター上で実行するメッセージ ストア プロバイダーを構成するユーザーをできるようにするインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="ed2ad-106">通常、メッセージ ストア プロバイダーは、ユーザーのプロファイルに追加するときに、メッセージ ストア プロバイダーが構成されます。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="ed2ad-107">メッセージ ストア プロバイダーの構成インターフェイスは一般にユーザー名とパスワードに必要なファイルへのパスを選択する、保護されたメッセージ ストアを設定するなどのタスクを処理し、基になるストレージ機構を作成するには、必要に応じて使用します。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="ed2ad-108">構成インターフェイスを実装するは、メッセージ サービス プロバイダーの DLL 内の他のエントリ ポイントを通じてアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="ed2ad-109">詳細については、[メッセージ サービスの構成](configuring-a-message-service.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="ed2ad-110">メッセージ ストア プロバイダーの構成のインターフェイスは、メッセージ ストア プロバイダーを実装する必要があります唯一のユーザー インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="ed2ad-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed2ad-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed2ad-111">See also</span></span>



<span data-ttu-id="ed2ad-112">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="ed2ad-112">[Message Store Features](message-store-features.md)</span></span>

