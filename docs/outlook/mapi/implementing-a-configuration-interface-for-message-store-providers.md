---
title: メッセージストアプロバイダー用の構成インターフェイスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332978"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="57e4f-103">メッセージストアプロバイダー用の構成インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="57e4f-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="57e4f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57e4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57e4f-105">メッセージストアプロバイダーは、ユーザーのコンピューター上で実行するようにメッセージストアプロバイダーを構成するためのインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e4f-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="57e4f-106">通常、メッセージストアプロバイダーは、メッセージストアプロバイダーがユーザーのプロファイルに追加されたときに構成されます。</span><span class="sxs-lookup"><span data-stu-id="57e4f-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="57e4f-107">メッセージストアプロバイダーの構成インターフェイスは、一般的に、保護されたメッセージストアのユーザー名とパスワードの設定、必要なファイルへのパスの選択、必要に応じた基礎となるストレージメカニズムの作成などのタスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="57e4f-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="57e4f-108">実装する構成インターフェイスは、メッセージサービスプロバイダーの DLL の追加エントリポイントを通じてアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="57e4f-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="57e4f-109">詳細については、「[メッセージサービスを構成](configuring-a-message-service.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57e4f-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="57e4f-110">メッセージストアプロバイダーの構成インターフェイスは、メッセージストアプロバイダーが実装する必要がある唯一のユーザーインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="57e4f-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57e4f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="57e4f-111">See also</span></span>



<span data-ttu-id="57e4f-112">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="57e4f-112">[Message Store Features](message-store-features.md)</span></span>

