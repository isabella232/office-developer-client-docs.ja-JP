---
title: '第 13 章: RDS の使用状況とセキュリティ'
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21f1484850a91d1fbdbe687f171e8ae9dfe4a5cd
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936470"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="862ec-102">第 13 章: RDS の使用状況とセキュリティ</span><span class="sxs-lookup"><span data-stu-id="862ec-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="862ec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="862ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="862ec-p101">ここでは、サーバーをセットアップしてすばやく RDS を使う方法について説明します。RDS の実装時に必要になることがある固有の構成手順や、RDS と他の技術との主要な関係について説明し、RDS ソリューションのセットアップ時に発生する問題の解決法を見いだすのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="862ec-p101">Use the information in this chapter to set up your server and use RDS quickly. This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="862ec-106">ここで説明する項目は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="862ec-106">This section contains information about:</span></span>

- [<span data-ttu-id="862ec-107">DataFactory の安全または無制限のモードの構成</span><span class="sxs-lookup"><span data-stu-id="862ec-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="862ec-108">RDS を構成する</span><span class="sxs-lookup"><span data-stu-id="862ec-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="862ec-109">IIS で仮想サーバーを構成します。</span><span class="sxs-lookup"><span data-stu-id="862ec-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="862ec-110">DataFactory のカスタマイズ (ADO)</span><span class="sxs-lookup"><span data-stu-id="862ec-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="862ec-111">DCOM を実行する DLL を有効にします。</span><span class="sxs-lookup"><span data-stu-id="862ec-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="862ec-112">[Web サーバー コンピューターにゲストの特権を付与します。RDS ゲストの特権\[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="862ec-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="862ec-113">ビジネス オブジェクトとしてスクリプト化の安全マーク</span><span class="sxs-lookup"><span data-stu-id="862ec-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="862ec-114">DCOM を使用については、クライアントのビジネス オブジェクトを登録して</span><span class="sxs-lookup"><span data-stu-id="862ec-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="862ec-115">RDS アプリケーションをセキュリティで保護します。</span><span class="sxs-lookup"><span data-stu-id="862ec-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="862ec-116">DCOM ストリーム マーシャ リングの形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="862ec-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="862ec-117">IIS でプロセッサごとのスレッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="862ec-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="862ec-118">RDS のトラブルシューティング (ADO)</span><span class="sxs-lookup"><span data-stu-id="862ec-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="862ec-119">RDS (ADO) に関連するテクノロジを使用します。</span><span class="sxs-lookup"><span data-stu-id="862ec-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)














