---
title: MAPI プロバイダーとコンポーネントの相互作用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434663"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="01416-103">MAPI プロバイダーとコンポーネントの相互作用</span><span class="sxs-lookup"><span data-stu-id="01416-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="01416-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01416-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01416-105">任意の種類の MAPI サービス プロバイダーは、他の MAPI コンポーネントを使用するには、特定のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="01416-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="01416-106">各サービス プロバイダーは、次の条件を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01416-106">Each service provider must:</span></span>
  
- <span data-ttu-id="01416-107">初期化には、適切なプロバイダー オブジェクトとログオン オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="01416-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="01416-108">初期化時に、プロバイダー エントリ ポイントのディスパッチ テーブルをメッセージング システムに返します。</span><span class="sxs-lookup"><span data-stu-id="01416-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="01416-109">プロバイダーが所有する各リソースの MAPI 状態テーブル行を登録し、適切な時間に [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01416-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="01416-110">有効な一意識別子 (UID) を取得するには [、IMAPISupport::NewUID](imapisupport-newuid.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="01416-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="01416-111">返されるオブジェクトの一般的な MAPI インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="01416-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="01416-112">MAPI メモリ割り当て関数を使用して、クライアント アプリケーションに返されるメモリを割り当て、MAPI サブシステムの他の部分によって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="01416-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="01416-113">必要に応じて、基になるメッセージング システムに資格情報を格納するプロファイル セクションを維持します。</span><span class="sxs-lookup"><span data-stu-id="01416-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="01416-114">[IMAPISupport::RegisterPreprocessor メソッド](imapisupport-registerpreprocessor.md)を使用して、メッセージの前処理関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="01416-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="01416-115">共通の定数、構造、インターフェイス、および戻り値を定義する適切なヘッダー ファイル (mapispi.h を含む) を含めます。</span><span class="sxs-lookup"><span data-stu-id="01416-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="01416-116">一般的なアドレスの種類については、アドレス形式の規則に従います。</span><span class="sxs-lookup"><span data-stu-id="01416-116">Follow address format conventions for common address types.</span></span>
    

