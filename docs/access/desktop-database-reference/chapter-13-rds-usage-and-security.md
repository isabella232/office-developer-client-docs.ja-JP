---
title: '第 13 章: RDS の使用とセキュリティ'
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c0753a53a2001a6c5c96ae2ceb801ee6eb75a5e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716020"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="633b6-102">第 13 章: RDS の使用とセキュリティ</span><span class="sxs-lookup"><span data-stu-id="633b6-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="633b6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="633b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="633b6-p101">ここでは、サーバーをセットアップしてすばやく RDS を使う方法について説明します。RDS の実装時に必要になることがある固有の構成手順や、RDS と他の技術との主要な関係について説明し、RDS ソリューションのセットアップ時に発生する問題の解決法を見いだすのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="633b6-p101">Use the information in this chapter to set up your server and use RDS quickly. This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="633b6-106">ここで説明する項目は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="633b6-106">This section contains information about:</span></span>

- [<span data-ttu-id="633b6-107">DataFactory をセーフ モードまたは無制限モードに設定する</span><span class="sxs-lookup"><span data-stu-id="633b6-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="633b6-108">RDS を構成する</span><span class="sxs-lookup"><span data-stu-id="633b6-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="633b6-109">IIS での仮想サーバーの構成</span><span class="sxs-lookup"><span data-stu-id="633b6-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="633b6-110">DataFactory のカスタマイズ (ADO)</span><span class="sxs-lookup"><span data-stu-id="633b6-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="633b6-111">DCOM で実行する DLL の有効化</span><span class="sxs-lookup"><span data-stu-id="633b6-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="633b6-112">[Web サーバー コンピューターにゲストの特権を付与します。RDS ゲストの特権\[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="633b6-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="633b6-113">スクリプト実行に安全なビジネス オブジェクトとしてマークする</span><span class="sxs-lookup"><span data-stu-id="633b6-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="633b6-114">DCOM を使用できるようにクライアント上にビジネス オブジェクトを登録する</span><span class="sxs-lookup"><span data-stu-id="633b6-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="633b6-115">RDS アプリケーションのセキュリティによる保護</span><span class="sxs-lookup"><span data-stu-id="633b6-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="633b6-116">DCOM ストリーム マーシャリング形式の設定</span><span class="sxs-lookup"><span data-stu-id="633b6-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="633b6-117">IIS でのプロセッサごとのスレッドの指定</span><span class="sxs-lookup"><span data-stu-id="633b6-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="633b6-118">RDS のトラブルシューティング (ADO)</span><span class="sxs-lookup"><span data-stu-id="633b6-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="633b6-119">RDS (ADO) に関連するテクノロジを使用します。</span><span class="sxs-lookup"><span data-stu-id="633b6-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)














