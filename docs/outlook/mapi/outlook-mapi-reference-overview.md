---
title: Outlook MAPI リファレンス概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '�ŏI�X�V��: 2013�N2��1��'
ms.openlocfilehash: bb7831ab79512eb8ca0018905e359654d7177cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564781"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="6544e-103">Outlook MAPI リファレンス概要</span><span class="sxs-lookup"><span data-stu-id="6544e-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="6544e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6544e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6544e-105">このトピックでは、Outlook 2013 MAPI のリファレンス ドキュメントの概要情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6544e-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="6544e-106">このマニュアルについて</span><span class="sxs-lookup"><span data-stu-id="6544e-106">About this documentation</span></span>

<span data-ttu-id="6544e-107">このドキュメントは、Microsoft Outlook 2013 でメッセージング API (MAPI) の実装に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6544e-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="6544e-108">Microsoft Office Outlook 2007 では、以前は、MAPI のプログラマーズ リファレンスは、Microsoft Exchange のドキュメントの一部をでした。</span><span class="sxs-lookup"><span data-stu-id="6544e-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6544e-109">Exchange は、MAPI の使用を Microsoft Exchange Server 2007 以降 deemphasized はため、Exchange の実装が制限されているをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6544e-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="6544e-110">MAPI の Outlook の実装は、Microsoft Exchange の実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6544e-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="6544e-111">Outlook の実装では、クライアント コンピューターで実行するために最適化し、低レイテンシを強調しています。</span><span class="sxs-lookup"><span data-stu-id="6544e-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="6544e-112">Exchange の実装は、サーバが高可用性と優れたマルチ スレッドが重要です。</span><span class="sxs-lookup"><span data-stu-id="6544e-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="6544e-113">エンド ・ ユーザーのシステムで実行するアプリケーションにこのドキュメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="6544e-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="6544e-114">サーバー アプリケーションでは、MAPI が該当する場合の Exchange の実装を使用して、または Exchange Web サービスなど、Exchange の現在の Api を使用します。</span><span class="sxs-lookup"><span data-stu-id="6544e-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="6544e-115">Exchange Web サービスの詳細については、 [Exchange Web サービスの参照](http://msdn.microsoft.com/en-us/library/bb204119.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6544e-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="6544e-116">MAPI、Outlook または Exchange の実装で動作するアプリケーションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6544e-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="6544e-117">など MFCMAPI は、両方のプラットフォームでうまく動作します。</span><span class="sxs-lookup"><span data-stu-id="6544e-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="6544e-118">実装は、多くの一般的な機能が明らかと微妙な違いがあります。</span><span class="sxs-lookup"><span data-stu-id="6544e-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="6544e-119">アプリケーションのすべての環境で動作する場合は、両方のプラットフォームで慎重にテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6544e-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="6544e-120">このテストにより、どちらの実装を実行して、同じオペレーティング システムのインストールではサポートされていないために、2 つのシステムが必要です。</span><span class="sxs-lookup"><span data-stu-id="6544e-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="6544e-121">MAPI は MAPI ストア内のデータへの低レベルのアクセスや、トランスポート、メッセージ ストアやアドレス帳プロバイダーを構築するために適切なことに注意します。</span><span class="sxs-lookup"><span data-stu-id="6544e-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="6544e-122">MAPI が Outlook のビジネス ロジックをバイパスするため、ソリューションを構築するための Api を評価するとき Outlook オブジェクト モデルの使用も考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6544e-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="6544e-123">Outlook オブジェクト モデルは Outlook のビジネス ロジックをカプセル化はしますが、マルチ スレッド コード、同期プロバイダー、または Windows サービス アプリケーションには適していません。</span><span class="sxs-lookup"><span data-stu-id="6544e-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="6544e-124">このエディションに新機能に関する情報については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6544e-124">For information about what is new in this edition, see the following topics:</span></span>
  
- <span data-ttu-id="6544e-125">[���̃o�[�W�����̐V�@�\���܂��B](what-s-new-in-this-edition.md)</span><span class="sxs-lookup"><span data-stu-id="6544e-125">[What's New in This Edition](what-s-new-in-this-edition.md)</span></span>
    
- [<span data-ttu-id="6544e-126">���� Edition �Ŕp�~���ꂽ API �v�f</span><span class="sxs-lookup"><span data-stu-id="6544e-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="6544e-127">Outlook の MAPI アプリケーションの開発に慣れていない場合は、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6544e-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="6544e-128">Outlook 2013 用のソリューションを開発するための API またはテクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="6544e-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- <span data-ttu-id="6544e-129">[�悭�g����w�b�_�[ �t�@�C��](commonly-used-header-files.md)</span><span class="sxs-lookup"><span data-stu-id="6544e-129">[Commonly Used Header Files](commonly-used-header-files.md)</span></span>
    
- [<span data-ttu-id="6544e-130">�悭�g�p�����v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="6544e-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="6544e-131">�悭�g�p�����I�u�W�F�N�g</span><span class="sxs-lookup"><span data-stu-id="6544e-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="6544e-132">この参照の残りの部分は、情報の次の 3 種類に分類されます。</span><span class="sxs-lookup"><span data-stu-id="6544e-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="6544e-133">[MAPI のサンプル](mapi-samples.md)では、API のさまざまな要素と基本の MAPI プロバイダーを実装して、Outlook アイテムを作成する方法の使用を示すコード サンプルが多数に指示します。</span><span class="sxs-lookup"><span data-stu-id="6544e-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="6544e-134">[MAPI の概念](mapi-concepts.md)には、MAPI のアーキテクチャと概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="6544e-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="6544e-135">[MAPI の参照](mapi-reference.md)では、関数、インターフェイス、構造体、および MAPI のプロパティに関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6544e-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6544e-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6544e-136">See also</span></span>

- [<span data-ttu-id="6544e-137">Outlook MAPI リファレンスの概要</span><span class="sxs-lookup"><span data-stu-id="6544e-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="6544e-138">MAPI Samples</span><span class="sxs-lookup"><span data-stu-id="6544e-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="6544e-139">MAPI �̊T�O</span><span class="sxs-lookup"><span data-stu-id="6544e-139">MAPI Concepts</span></span>](mapi-concepts.md)

