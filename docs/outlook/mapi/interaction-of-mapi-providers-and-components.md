---
title: MAPI プロバイダーとコンポーネントの相互作用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592627"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="34732-103">MAPI プロバイダーとコンポーネントの相互作用</span><span class="sxs-lookup"><span data-stu-id="34732-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="34732-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34732-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34732-105">どのような種類の MAPI サービス プロバイダーは、その他の MAPI コンポーネントを操作する特定のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="34732-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="34732-106">各サービス プロバイダーにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="34732-106">Each service provider must:</span></span>
  
- <span data-ttu-id="34732-107">初期化のため、適切なプロバイダー オブジェクトとログオン オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="34732-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="34732-108">メッセージング システムの初期化時にプロバイダーのエントリ ポイントのディスパッチ テーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="34732-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="34732-109">リソースごとに、プロバイダーによって所有されている MAPI の状態テーブルの行を登録し、適切な時点で、 [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="34732-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="34732-110">[IMAPISupport::NewUID](imapisupport-newuid.md)メソッドを使用して、有効な一意の識別子 (Uid) を取得します。</span><span class="sxs-lookup"><span data-stu-id="34732-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="34732-111">返すオブジェクトの一般的な MAPI インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="34732-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="34732-112">MAPI のメモリ割り当て関数を使用して、クライアント アプリケーションに返されるメモリを割り当てると、MAPI サブシステムの他の部分によって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="34732-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="34732-113">必要に応じて、基になるメッセージング システムに資格情報を格納するプロファイル] セクションを維持します。</span><span class="sxs-lookup"><span data-stu-id="34732-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="34732-114">関数を処理するすべてのメッセージを登録するのには、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="34732-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="34732-115">一般的な定数、構造体、インターフェイスを定義し、値を返す適切なヘッダー ファイル (mapispi.h など) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="34732-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="34732-116">アドレスのアドレスの種類の一般的な書体の表記規則に従います。</span><span class="sxs-lookup"><span data-stu-id="34732-116">Follow address format conventions for common address types.</span></span>
    

