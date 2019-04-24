---
title: Visio のセキュリティ設定とコードの実行について (シェイプシート)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
localization_priority: Normal
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。
ms.openlocfilehash: 72b4a45faa46778b7a369cfe458ee4e0e9ea71bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345025"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a><span data-ttu-id="28591-105">Visio のセキュリティ設定とコードの実行について (シェイプシート)</span><span class="sxs-lookup"><span data-stu-id="28591-105">About Security Settings and Running Code in Visio (ShapeSheet)</span></span>

 <span data-ttu-id="28591-106">セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="28591-106">Creating secure applications is one of the primary challenges facing solution developers.</span></span> <span data-ttu-id="28591-107">ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。</span><span class="sxs-lookup"><span data-stu-id="28591-107">Users, administrators, and developers are increasingly aware of the potential of unknowingly running code that can be harmful to their computers.</span></span> <span data-ttu-id="28591-108">アプリケーションの整合性を確保することはいっそう重要になっています。</span><span class="sxs-lookup"><span data-stu-id="28591-108">It is more important than ever that you help to ensure the integrity of your applications.</span></span> 
  
<span data-ttu-id="28591-109">すべてのセキュリティ設定は Office 全体であり、セキュリティ**センター**で設定されます ([**ファイル**] タブをクリックし、[**オプション**] をクリックして、[セキュリティ**センター**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="28591-109">All security settings are Office-wide and are set in the **Trust Center** (click the **File** tab, click **Options**, and then click **Trust Center**).</span></span> <span data-ttu-id="28591-110">影響を受ける設定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="28591-110">Affected settings include the following:</span></span>
  
- <span data-ttu-id="28591-111">信頼できるパブリッシャーの指定</span><span class="sxs-lookup"><span data-stu-id="28591-111">Specifying trusted publishers</span></span>
    
- <span data-ttu-id="28591-112">信頼できる場所の指定</span><span class="sxs-lookup"><span data-stu-id="28591-112">Specifying trusted locations</span></span>
    
- <span data-ttu-id="28591-113">COM アドインの読み込み</span><span class="sxs-lookup"><span data-stu-id="28591-113">Loading COM add-ins</span></span> 
    
- <span data-ttu-id="28591-114">発行され、パスが検出されたアドオンの読み込み</span><span class="sxs-lookup"><span data-stu-id="28591-114">Loading published and path-discovered add-ons</span></span>
    
- <span data-ttu-id="28591-115">VBA マクロの読み込み</span><span class="sxs-lookup"><span data-stu-id="28591-115">Loading VBA macros</span></span>
    
<span data-ttu-id="28591-116">以前のバージョンの Visio では、設定は [**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。</span><span class="sxs-lookup"><span data-stu-id="28591-116">In previous versions of Visio, settings were made in the **Security** dialog box and the **Security** tab of the **Options** dialog box (**Tools** menu).</span></span> <span data-ttu-id="28591-117">Office visio 2007 では、これらのダイアログボックスは廃止され、Microsoft visio 2010 の場合、visio のツールバーとメニューはリボンに置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="28591-117">As of Office Visio 2007, these dialog boxes have been eliminated, and as of Microsoft Visio 2010, Visio toolbars and menus have been replaced by the ribbon.</span></span> 
  
<span data-ttu-id="28591-118">Office**セキュリティセンター**の設定の詳細については、「 [Microsoft office ソリューション開発者向けのセキュリティに関する注意事項](https://msdn.microsoft.com/en-us/library/aa433259.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28591-118">For more information about settings in the Office **Trust Center**, see [Security Notes for Microsoft Office Solution Developers](https://msdn.microsoft.com/en-us/library/aa433259.aspx).</span></span>
  
 <span data-ttu-id="28591-119">デジタル署名コード、信頼のおける発行元、発行元に関する情報については、MSDN (Microsoft Developer Network web サイト) の「コード署名」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="28591-119">For information about digitally signing code and trusted sources and publishers, search for "code signing" on MSDN, the Microsoft Developer Network website.</span></span> 
  
<span data-ttu-id="28591-120">適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="28591-120">For more information about good security design practices and technologies, search for "security" on MSDN.</span></span> 
  
## <a name="additional-visio-resources"></a><span data-ttu-id="28591-121">Visio の追加リソース</span><span class="sxs-lookup"><span data-stu-id="28591-121">Additional Visio resources</span></span>

- <span data-ttu-id="28591-122">visio アドオンと com アドインの詳細については、MSDN の記事「 [visio 2007 でのアドオンと com アドインの概要](https://msdn.microsoft.com/library/bb851468.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28591-122">To learn more about Visio add-ons and COM add-ins, see the MSDN article, [Overview of Add-ons and COM Add-ins in Visio 2007](https://msdn.microsoft.com/library/bb851468.aspx).</span></span>
    
- <span data-ttu-id="28591-123">RUNADDON 関数と**AddonName**プロパティの詳細については、MSDN の記事「 [RUNADDON 関数での変更点」および「AddonName プロパティ (Visio 2002](https://msdn.microsoft.com/library/aa140368%28office.10%29.aspx))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28591-123">To learn more about the RUNADDON function and the **AddonName** property, see the MSDN article [Changes in the RUNADDON Function and the AddOnName Property for Visio 2002](https://msdn.microsoft.com/library/aa140368%28office.10%29.aspx).</span></span>
    

