---
title: Outlook ソーシャル コネクタ プロバイダー インターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook ソーシャル コネクタ (OSC) では、Office 機能 Office クライアント アプリケーションで共有社会に接続して、ビジネス ネットワークは、Office を離れることがなく、ネットワーク内のユーザーをユーザーが維持できるようにするためです。
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804456"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="f5386-103">Outlook ソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f5386-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="f5386-104">Outlook ソーシャル コネクタ (OSC) では、Office 機能 Office クライアント アプリケーションで共有社会に接続して、ビジネス ネットワークは、Office を離れることがなく、ネットワーク内のユーザーをユーザーが維持できるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="f5386-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="f5386-105">OSC プロバイダーでは、コンポーネント オブジェクト モデル (COM) DLL の各ソーシャル ネットワークの Api に依存しない方法でデータをソーシャル ネットワークにアクセスする OSC を可能にします。</span><span class="sxs-lookup"><span data-stu-id="f5386-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="f5386-106">次の表は、OSC プロバイダーの拡張機能でインターフェイスを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="f5386-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="f5386-107">OSC プロバイダーは、OSC と通信するのには 5 つのインタ フェースの 4 つを実装する必要が: [ISocialPerson](isocialpersoniunknown.md)、 [ISocialProfile](isocialprofileisocialperson.md)、 [ISocialProvider](isocialprovideriunknown.md)、および[ISocialSession](isocialsessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="f5386-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="f5386-108">OSC プロバイダーは、同期アクティビティ、オン ・ デマンドをサポートしている場合、または資格情報、または個人を追跡する機能にキャッシュされたログオン資格情報をキャッシュしを使用してログオンするときに、友人のハイブリッド同期プロバイダーは、 [ISocialSession2 を実装する必要があります。](isocialsession2iunknown.md)も同様です。</span><span class="sxs-lookup"><span data-stu-id="f5386-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="f5386-109">**名前**</span><span class="sxs-lookup"><span data-stu-id="f5386-109">**Name**</span></span>|<span data-ttu-id="f5386-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="f5386-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5386-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="f5386-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="f5386-112">ソーシャル ネットワーク上のユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="f5386-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="f5386-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="f5386-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="f5386-114">ユーザーのログオンを表します。</span><span class="sxs-lookup"><span data-stu-id="f5386-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="f5386-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="f5386-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="f5386-116">OSC プロバイダーのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="f5386-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="f5386-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="f5386-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="f5386-118">ソーシャル ネットワーク サイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="f5386-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="f5386-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="f5386-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="f5386-120">友人を追加する、アクティビティの同期をサポートするオン ・ デマンドまたはハイブリッドの同期の友人、またはを使用して、ソーシャル ネットワークへのログオンにキャッシュされた資格情報。</span><span class="sxs-lookup"><span data-stu-id="f5386-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

