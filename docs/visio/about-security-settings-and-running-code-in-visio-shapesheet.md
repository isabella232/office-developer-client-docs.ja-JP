---
title: Visio のセキュリティ設定とコードの実行について (シェイプシート)
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
localization_priority: Normal
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行する可能性をますます認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。
ms.openlocfilehash: 3ad2aef9096ad2ad344b2d6fb22ed610756916bb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819267"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a><span data-ttu-id="97820-105">Visio のセキュリティ設定とコードの実行について (シェイプシート)</span><span class="sxs-lookup"><span data-stu-id="97820-105">About Security Settings and Running Code in Visio (ShapeSheet)</span></span>

 <span data-ttu-id="97820-106">セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="97820-106">Creating secure applications is one of the primary challenges facing solution developers.</span></span> <span data-ttu-id="97820-107">ユーザー、管理者、開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行する可能性をますます認識しています。</span><span class="sxs-lookup"><span data-stu-id="97820-107">Users, administrators, and developers are increasingly aware of the potential of unknowingly running code that can be harmful to their computers.</span></span> <span data-ttu-id="97820-108">アプリケーションの整合性を確保することはいっそう重要になっています。</span><span class="sxs-lookup"><span data-stu-id="97820-108">It is more important than ever that you help to ensure the integrity of your applications.</span></span> 
  
<span data-ttu-id="97820-109">すべてのセキュリティ設定はOffice全体に設定され、セキュリティ センターで設定 **されます ([** ファイル] タブをクリックし、[オプション] をクリックし、[セキュリティ センター]**をクリックします**)。</span><span class="sxs-lookup"><span data-stu-id="97820-109">All security settings are Office-wide and are set in the **Trust Center** (click the **File** tab, click **Options**, and then click **Trust Center**).</span></span> <span data-ttu-id="97820-110">影響を受ける設定には、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="97820-110">Affected settings include the following:</span></span>
  
- <span data-ttu-id="97820-111">信頼できるパブリッシャーの指定</span><span class="sxs-lookup"><span data-stu-id="97820-111">Specifying trusted publishers</span></span>
    
- <span data-ttu-id="97820-112">信頼できる場所の指定</span><span class="sxs-lookup"><span data-stu-id="97820-112">Specifying trusted locations</span></span>
    
- <span data-ttu-id="97820-113">COM アドインの読み込み</span><span class="sxs-lookup"><span data-stu-id="97820-113">Loading COM add-ins</span></span> 
    
- <span data-ttu-id="97820-114">発行され、パスが検出されたアドオンの読み込み</span><span class="sxs-lookup"><span data-stu-id="97820-114">Loading published and path-discovered add-ons</span></span>
    
- <span data-ttu-id="97820-115">VBA マクロの読み込み</span><span class="sxs-lookup"><span data-stu-id="97820-115">Loading VBA macros</span></span>
    
<span data-ttu-id="97820-116">以前のバージョンの Visio では、設定は [**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。</span><span class="sxs-lookup"><span data-stu-id="97820-116">In previous versions of Visio, settings were made in the **Security** dialog box and the **Security** tab of the **Options** dialog box (**Tools** menu).</span></span> <span data-ttu-id="97820-117">Office Visio 2007 年現在、これらのダイアログ ボックスは削除され、Microsoft Visio 2010 では、Visio ツールバーとメニューがリボンに置き換えされています。</span><span class="sxs-lookup"><span data-stu-id="97820-117">As of Office Visio 2007, these dialog boxes have been eliminated, and as of Microsoft Visio 2010, Visio toolbars and menus have been replaced by the ribbon.</span></span> 
  
<span data-ttu-id="97820-118">セキュリティ センターの設定の詳細については、「Office **ソリューション** 開発者向け [セキュリティ Microsoft Officeを参照してください](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa433259(v=office.12))。</span><span class="sxs-lookup"><span data-stu-id="97820-118">For more information about settings in the Office **Trust Center**, see [Security Notes for Microsoft Office Solution Developers](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa433259(v=office.12)).</span></span>
  
 <span data-ttu-id="97820-119">デジタル署名コードと信頼できるソースと発行元の詳細については、MSDN の web サイトで "コード署名" をMicrosoft Developer Networkしてください。</span><span class="sxs-lookup"><span data-stu-id="97820-119">For information about digitally signing code and trusted sources and publishers, search for "code signing" on MSDN, the Microsoft Developer Network website.</span></span> 
  
<span data-ttu-id="97820-120">適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="97820-120">For more information about good security design practices and technologies, search for "security" on MSDN.</span></span> 
  
## <a name="additional-visio-resources"></a><span data-ttu-id="97820-121">Visio の追加リソース</span><span class="sxs-lookup"><span data-stu-id="97820-121">Additional Visio resources</span></span>

- <span data-ttu-id="97820-122">Visio アドオンと COM アドインの詳細については、MSDN の記事「Visio [2007](https://docs.microsoft.com/previous-versions/office/developer/office-2007/bb851468(v=office.12))のアドオンと COM アドインの概要」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97820-122">To learn more about Visio add-ons and COM add-ins, see the MSDN article, [Overview of Add-ons and COM Add-ins in Visio 2007](https://docs.microsoft.com/previous-versions/office/developer/office-2007/bb851468(v=office.12)).</span></span>
    
- <span data-ttu-id="97820-123">RUNADDON 関数と **AddonName** プロパティの詳細については、MSDN の記事「RUNADDON 関数の変更点」および「AddOnName プロパティ for Visio [2002」を参照](https://docs.microsoft.com/previous-versions/office/developer/office-xp/aa140368(v=office.10))してください。</span><span class="sxs-lookup"><span data-stu-id="97820-123">To learn more about the RUNADDON function and the **AddonName** property, see the MSDN article [Changes in the RUNADDON Function and the AddOnName Property for Visio 2002](https://docs.microsoft.com/previous-versions/office/developer/office-xp/aa140368(v=office.10)).</span></span>
    

