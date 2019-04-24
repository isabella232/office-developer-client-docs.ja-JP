---
title: MAPI アドレス帳プロバイダーの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316703"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="d46b5-103">MAPI アドレス帳プロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="d46b5-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="d46b5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d46b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d46b5-105">アドレス帳プロバイダーは、クライアントアプリケーション、メッセージストアとトランスポートプロバイダー、MAPI に受信者情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="d46b5-106">受信者情報は、コンテナーと呼ばれる記憶域コンパートメントに階層的に編成されます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="d46b5-107">プロファイル内のすべてのアドレス帳は、1つまたは複数の最上位レベルまたは親コンテナーに MAPI アドレス帳を提供します。これにより、セッション内のすべてのアドレス帳プロバイダーからの受信者情報が統合されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="d46b5-108">クライアントやその他のサービスプロバイダーがアドレス帳プロバイダーのデータにアクセスできるようにするには、MAPI アドレス帳を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d46b5-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="d46b5-109">MAPI は、次の方法で統合アドレス帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="d46b5-110">各アドレス帳プロバイダーからトップレベルのコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="d46b5-111">各コンテナーの階層テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="d46b5-112">各階層テーブルを統合階層テーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d46b5-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="d46b5-113">これは、クライアントに公開される統合階層テーブルです。</span><span class="sxs-lookup"><span data-stu-id="d46b5-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="d46b5-114">MAPI では、アドレス帳プロバイダーの作成者に対して、いくつかの要件があります。</span><span class="sxs-lookup"><span data-stu-id="d46b5-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="d46b5-115">アドレス帳の作成者として実装できる機能の範囲はさまざまで、柔軟性に富んでいます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="d46b5-116">たとえば、プロバイダーは、特定の種類の受信者情報の読み取り専用ビューを提供すること、または機能の完全なセットを実装することに制限されている可能性があります。これにより、クライアントまたはプロバイダーが受信者データを追加または変更することができます。カスタマイズされたビューを定義するための検索条件。</span><span class="sxs-lookup"><span data-stu-id="d46b5-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="d46b5-117">プロバイダーのデータは、ファイル、データベース、またはリモートサーバーにローカルに配置できます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="d46b5-118">アドレス帳プロバイダーによっては、特定のメッセージングシステムを使用して、トランスポートプロバイダーと密に結合しているものがあります。また、その他のプロバイダーは任意のメッセージングシステムで動作します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="d46b5-119">MAPI は、1つの変更可能なコンテナーを実装し、他のコンテナーからコピーした受信者情報と、直接作成された情報を保持できる、個人用アドレス帳、または PAB と呼ばれる特別な種類のアドレス帳プロバイダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="d46b5-120">任意のアドレス帳プロバイダーで pab を実装して、複数の PABs をプロファイルに追加できますが、1つのセッション中に pab として動作するように指定できるのはこれらのプロバイダーの1つだけです。</span><span class="sxs-lookup"><span data-stu-id="d46b5-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

