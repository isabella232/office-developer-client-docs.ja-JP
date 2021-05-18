---
title: Outlookソーシャル コネクタ プロバイダー インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook ソーシャル コネクタ (OSC) は、Office クライアント アプリケーションが共有する Office 機能で、ソーシャル ネットワークやビジネス ネットワークに接続し、ユーザーが Office を離れることなくネットワーク内のユーザーと連絡を取り合える機能です。
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422811"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="5efef-103">Outlookソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5efef-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="5efef-104">Outlook ソーシャル コネクタ (OSC) は、Office クライアント アプリケーションが共有する Office 機能で、ソーシャル ネットワークやビジネス ネットワークに接続し、ユーザーが Office を離れることなくネットワーク内のユーザーと連絡を取り合える機能です。</span><span class="sxs-lookup"><span data-stu-id="5efef-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="5efef-105">OSC プロバイダーはコンポーネント オブジェクト モデル (COM) DLL で、各ソーシャル ネットワークの API とは独立した方法で OSC がソーシャル ネットワーク データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5efef-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="5efef-106">次の表に、OSC プロバイダーの機能拡張のインターフェイスを示します。</span><span class="sxs-lookup"><span data-stu-id="5efef-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="5efef-107">OSC プロバイダーは、5 つのインターフェイスの 4 つを実装して OSC と通信する必要があります[。ISocialPerson](isocialpersoniunknown.md) [、ISocialProfile、ISocialProvider、](isocialprofileisocialperson.md)[および ISocialSession](isocialsessioniunknown.md)です。 [](isocialprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="5efef-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="5efef-108">OSC プロバイダーがアクティビティの同期、フレンドのオンデマンドまたはハイブリッド同期、ログオン資格情報のキャッシュ、キャッシュされた資格情報の使用、またはユーザーのフォロー機能をサポートしている場合、プロバイダーは [ISocialSession2](isocialsession2iunknown.md)も実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5efef-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="5efef-109">**名前**</span><span class="sxs-lookup"><span data-stu-id="5efef-109">**Name**</span></span>|<span data-ttu-id="5efef-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="5efef-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5efef-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="5efef-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="5efef-112">ソーシャル ネットワーク上のユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="5efef-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="5efef-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="5efef-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="5efef-114">ログオンしているユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="5efef-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="5efef-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="5efef-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="5efef-116">OSC プロバイダーのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="5efef-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="5efef-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="5efef-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="5efef-118">ソーシャル ネットワーク サイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="5efef-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="5efef-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="5efef-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="5efef-120">キャッシュされた資格情報を使用して、アクティビティの同期、友人の追加、フレンドのオンデマンドまたはハイブリッド同期、またはソーシャル ネットワークへのログオンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5efef-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

