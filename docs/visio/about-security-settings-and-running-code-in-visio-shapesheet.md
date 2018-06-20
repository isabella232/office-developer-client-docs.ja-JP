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
description: セキュリティで保護されたアプリケーションを作成すると、ソリューション開発者が直面する主な課題の 1 つです。 ユーザー、管理者、および開発者は、自分のコンピューターに問題を引き起こすことができるコードを無意識に実行する可能性を徐々 に認識します。 重要ですこれまでよりも、アプリケーションの整合性を確保することができます。
ms.openlocfilehash: e114fef650f31a6e0adf368d339f71e3a32113f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804730"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a><span data-ttu-id="c7a8e-105">Visio のセキュリティ設定とコードの実行について (シェイプシート)</span><span class="sxs-lookup"><span data-stu-id="c7a8e-105">About Security Settings and Running Code in Visio (ShapeSheet)</span></span>

 <span data-ttu-id="c7a8e-106">セキュリティで保護されたアプリケーションを作成すると、ソリューション開発者が直面する主な課題の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-106">Creating secure applications is one of the primary challenges facing solution developers.</span></span> <span data-ttu-id="c7a8e-107">ユーザー、管理者、および開発者は、自分のコンピューターに問題を引き起こすことができるコードを無意識に実行する可能性を徐々 に認識します。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-107">Users, administrators, and developers are increasingly aware of the potential of unknowingly running code that can be harmful to their computers.</span></span> <span data-ttu-id="c7a8e-108">重要ですこれまでよりも、アプリケーションの整合性を確保することができます。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-108">It is more important than ever that you help to ensure the integrity of your applications.</span></span> 
  
<span data-ttu-id="c7a8e-109">すべてのセキュリティ設定は**セキュリティ センター**の設定は、Office 全体 (、[**ファイル**] タブをクリックして、**オプション**] をクリックし、[**セキュリティ センター**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-109">All security settings are Office-wide and are set in the **Trust Center** (click the **File** tab, click **Options**, and then click **Trust Center**).</span></span> <span data-ttu-id="c7a8e-110">影響を受ける設定を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-110">Affected settings include the following:</span></span>
  
- <span data-ttu-id="c7a8e-111">信頼できるパブリッシャーの指定</span><span class="sxs-lookup"><span data-stu-id="c7a8e-111">Specifying trusted publishers</span></span>
    
- <span data-ttu-id="c7a8e-112">信頼できる場所の指定</span><span class="sxs-lookup"><span data-stu-id="c7a8e-112">Specifying trusted locations</span></span>
    
- <span data-ttu-id="c7a8e-113">COM アドインの読み込み</span><span class="sxs-lookup"><span data-stu-id="c7a8e-113">Loading COM add-ins</span></span> 
    
- <span data-ttu-id="c7a8e-114">発行され、パスが検出されたアドオンの読み込み</span><span class="sxs-lookup"><span data-stu-id="c7a8e-114">Loading published and path-discovered add-ons</span></span>
    
- <span data-ttu-id="c7a8e-115">VBA マクロの読み込み</span><span class="sxs-lookup"><span data-stu-id="c7a8e-115">Loading VBA macros</span></span>
    
<span data-ttu-id="c7a8e-116">Visio の以前のバージョンでは、設定は、[**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-116">In previous versions of Visio, settings were made in the **Security** dialog box and the **Security** tab of the **Options** dialog box (**Tools** menu).</span></span> <span data-ttu-id="c7a8e-117">Office Visio 2007 では、現在これらのダイアログ ボックスが除去され、Microsoft Visio 2010 では、現在の Visio ツールバーとメニューに置き換えられているリボンです。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-117">As of Office Visio 2007, these dialog boxes have been eliminated, and as of Microsoft Visio 2010, Visio toolbars and menus have been replaced by the ribbon.</span></span> 
  
<span data-ttu-id="c7a8e-118">Office**セキュリティ センター**の設定の詳細については、 [Microsoft Office ソリューション開発者向けのセキュリティ ノート](http://msdn2.microsoft.com/en-us/library/aa433259.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-118">For more information about settings in the Office **Trust Center**, see [Security Notes for Microsoft Office Solution Developers](http://msdn2.microsoft.com/en-us/library/aa433259.aspx).</span></span>
  
 <span data-ttu-id="c7a8e-119">デジタル署名コード、信頼のおける発行元、発行側に関する詳細については、MSDN (Microsoft Developer Network) Web サイト上で「コード署名」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-119">For information about digitally signing code and trusted sources and publishers, search for "code signing" on MSDN, the Microsoft Developer Network Web site.</span></span> 
  
<span data-ttu-id="c7a8e-120">適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-120">For more information about good security design practices and technologies, search for "security" on MSDN.</span></span> 
  
## <a name="additional-visio-resources"></a><span data-ttu-id="c7a8e-121">Visio の追加リソース</span><span class="sxs-lookup"><span data-stu-id="c7a8e-121">Additional Visio resources</span></span>

- <span data-ttu-id="c7a8e-122">Visio アドオンおよび COM アドインに関する詳細については、[概要のアドオンおよび COM アドインで Visio 2007](http://msdn.microsoft.com/en-us/library/bb851468.aspx)は、MSDN の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-122">To learn more about Visio add-ons and COM add-ins, see the MSDN article, [Overview of Add-ons and COM Add-ins in Visio 2007](http://msdn.microsoft.com/en-us/library/bb851468.aspx).</span></span>
    
- <span data-ttu-id="c7a8e-123">RUNADDON 関数および**AddonName**プロパティの詳細については、MSDN の記事[によって、RUNADDON 関数および AddOnName プロパティ Visio 2002 での変更](http://msdn.microsoft.com/en-us/library/aa140368%28office.10%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7a8e-123">To learn more about the RUNADDON function and the **AddonName** property, see the MSDN article [Changes in the RUNADDON Function and the AddOnName Property for Visio 2002](http://msdn.microsoft.com/en-us/library/aa140368%28office.10%29.aspx).</span></span>
    

