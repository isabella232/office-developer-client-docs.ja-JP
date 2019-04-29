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
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="453cf-103">MAPI プロバイダーとコンポーネントの相互作用</span><span class="sxs-lookup"><span data-stu-id="453cf-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="453cf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="453cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="453cf-105">すべての種類の mapi サービスプロバイダーは、特定のガイドラインに従って他の mapi コンポーネントと連携する必要があります。</span><span class="sxs-lookup"><span data-stu-id="453cf-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="453cf-106">各サービスプロバイダーは次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="453cf-106">Each service provider must:</span></span>
  
- <span data-ttu-id="453cf-107">適切なプロバイダーおよびログオンオブジェクトを使用して初期化を行います。</span><span class="sxs-lookup"><span data-stu-id="453cf-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="453cf-108">初期化時に、プロバイダーエントリポイントのディスパッチテーブルをメッセージングシステムに返します。</span><span class="sxs-lookup"><span data-stu-id="453cf-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="453cf-109">プロバイダーが所有する各リソースに対して MAPI 状態テーブル行を登録し、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを適切な時刻に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="453cf-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="453cf-110">有効な一意識別子 (uid) を取得するには、 [imapisupport:: newuid](imapisupport-newuid.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="453cf-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="453cf-111">返されるオブジェクトの一般的な MAPI インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="453cf-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="453cf-112">mapi メモリ割り当て関数を使用して、クライアントアプリケーションに返されるメモリを割り当て、mapi サブシステムの他の部分によって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="453cf-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="453cf-113">必要に応じて、基になるメッセージングシステムに資格情報を格納するために、プロファイルセクションを維持します。</span><span class="sxs-lookup"><span data-stu-id="453cf-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="453cf-114">[imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドを使用して、任意のメッセージプリプロセス関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="453cf-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="453cf-115">一般的な定数、構造体、インターフェイス、および戻り値を定義する適切なヘッダーファイル (mapispi を含む) を含めます。</span><span class="sxs-lookup"><span data-stu-id="453cf-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="453cf-116">一般的なアドレスの種類のアドレス形式の規則に従います。</span><span class="sxs-lookup"><span data-stu-id="453cf-116">Follow address format conventions for common address types.</span></span>
    

