---
title: cancelrecordchange マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: CancelRecordChange/レコードの変更の取り消しアクションを使用して、変更を確定する前に CreateRecord または EditRecord データ ブロック内でレコードに適用した変更を取り消すことができます。
ms.openlocfilehash: fe95718e752513c4b8b700f331fec7b78092e553
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411828"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="f5399-103">cancelrecordchange マクロアクション (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="f5399-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f5399-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span><span class="sxs-lookup"><span data-stu-id="f5399-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f5399-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="f5399-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f5399-107">"**CancelRecordChange/レコードの変更の取り消し**" アクションは、データ マクロ内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f5399-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f5399-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f5399-108">Remarks</span></span>

<span data-ttu-id="f5399-109">"**CancelRecordChange/レコードの変更の取り消し**" アクションを呼び出すと、**CreateRecord** データ ブロックまたは **EditRecord** データ ブロックは即座に終了します。</span><span class="sxs-lookup"><span data-stu-id="f5399-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  

