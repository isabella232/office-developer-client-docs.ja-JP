---
title: Outlook Social Connector プロバイダーインターフェイス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (.osc) は、office クライアントアプリケーションによってソーシャルおよびビジネスネットワークに接続され、ユーザーが office を離れずにネットワーク内のユーザーと連絡を取り合うことができるようにする office の機能です。
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359851"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="38998-103">Outlook Social Connector プロバイダーインターフェイス</span><span class="sxs-lookup"><span data-stu-id="38998-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="38998-104">Outlook Social Connector (.osc) は、office クライアントアプリケーションによってソーシャルおよびビジネスネットワークに接続され、ユーザーが office を離れずにネットワーク内のユーザーと連絡を取り合うことができるようにする office の機能です。</span><span class="sxs-lookup"><span data-stu-id="38998-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="38998-105">.osc プロバイダーは、コンポーネントオブジェクトモデル (COM) DLL で、各ソーシャルネットワークの api とは無関係に、.osc がソーシャルネットワークデータにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="38998-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="38998-106">次の表に、.osc プロバイダ拡張機能のインターフェイスを示します。</span><span class="sxs-lookup"><span data-stu-id="38998-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="38998-107">.osc プロバイダーは、.osc と通信するために、次の5つのインターフェイスを実装する必要があります。 i入力された[alperson](isocialpersoniunknown.md)、 [i通達 alprofile](isocialprofileisocialperson.md)、 [isocialperson](isocialprovideriunknown.md)、および[i指定 alsession](isocialsessioniunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="38998-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="38998-108">.osc プロバイダーが、フレンドの同期アクティビティ、オンデマンドまたはハイブリッド同期、ログイン資格情報のキャッシュ、キャッシュされた資格情報を使用したログオン、または個人をフォローする機能をサポートしている場合は、プロバイダーは ISocialSession2 を実装する必要があります。 [](isocialsession2iunknown.md)も同様です。</span><span class="sxs-lookup"><span data-stu-id="38998-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="38998-109">**[名前]**</span><span class="sxs-lookup"><span data-stu-id="38998-109">**Name**</span></span>|<span data-ttu-id="38998-110">**[説明]**</span><span class="sxs-lookup"><span data-stu-id="38998-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38998-111">i社会</span><span class="sxs-lookup"><span data-stu-id="38998-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="38998-112">ソーシャルネットワーク上の人物を表します。</span><span class="sxs-lookup"><span data-stu-id="38998-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="38998-113">iこの alprofile</span><span class="sxs-lookup"><span data-stu-id="38998-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="38998-114">ログオンしているユーザーを表します。</span><span class="sxs-lookup"><span data-stu-id="38998-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="38998-115">iこの alprovider</span><span class="sxs-lookup"><span data-stu-id="38998-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="38998-116">.osc プロバイダーのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="38998-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="38998-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="38998-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="38998-118">ソーシャルネットワークサイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="38998-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="38998-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="38998-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="38998-120">アクティビティの同期、フレンドの追加、オンデマンドまたはハイブリッド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38998-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

