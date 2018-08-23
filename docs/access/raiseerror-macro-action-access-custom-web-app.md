---
title: RaiseError マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: RaiseError /エラーの生成アクションは、指定されたエラー メッセージが含まれるポップアップ ウィンドウを表示します。
ms.openlocfilehash: 1176804106c5cfd9d4bd30f79f47975593089dbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798721"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="59bd2-103">RaiseError マクロ アクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="59bd2-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="59bd2-104">" **RaiseError** /エラーの生成" アクションは、指定されたエラー メッセージが含まれるポップアップ ウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="59bd2-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="59bd2-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="59bd2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="59bd2-107">[!メモ] " **RaiseError** /エラーの生成" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="59bd2-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="59bd2-108">設定</span><span class="sxs-lookup"><span data-stu-id="59bd2-108">Setting</span></span>

<span data-ttu-id="59bd2-109">" **RaiseError** /エラーの生成" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="59bd2-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="59bd2-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="59bd2-110">**Argument**</span></span>|<span data-ttu-id="59bd2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="59bd2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="59bd2-112">_エラーの説明_</span><span class="sxs-lookup"><span data-stu-id="59bd2-112">_Error Description_</span></span> <br/> |<span data-ttu-id="59bd2-113">エラーを説明する文字列式。</span><span class="sxs-lookup"><span data-stu-id="59bd2-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59bd2-114">注釈</span><span class="sxs-lookup"><span data-stu-id="59bd2-114">Remarks</span></span>

<span data-ttu-id="59bd2-115">" **RaiseError** /エラーの生成" アクションが呼び出されると、現在のトランザクションのすべての操作がロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="59bd2-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

