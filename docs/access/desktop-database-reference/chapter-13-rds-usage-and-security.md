---
title: '第 13 章: RDS の使用とセキュリティ'
TOCTitle: 'Chapter 13: RDS Usage and Security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4250235d433572944d311611c909c060d2e69da9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876107"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="30792-102">第 13 章: RDS の使用とセキュリティ</span><span class="sxs-lookup"><span data-stu-id="30792-102">Chapter 13: RDS Usage and Security</span></span>


<span data-ttu-id="30792-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="30792-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30792-p101">ここでは、サーバーをセットアップしてすばやく RDS を使う方法について説明します。RDS の実装時に必要になることがある固有の構成手順や、RDS と他の技術との主要な関係について説明し、RDS ソリューションのセットアップ時に発生する問題の解決法を見いだすのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="30792-p101">Use the information in this chapter to set up your server and use RDS quickly. This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="30792-106">ここで説明する項目は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="30792-106">This section contains information about:</span></span>

- [<span data-ttu-id="30792-107">RDS を構成する</span><span class="sxs-lookup"><span data-stu-id="30792-107">Configuring RDS</span></span>](configuring-rds.md)

- <span data-ttu-id="30792-108">[Web サーバー コンピューターにゲストの特権を付与します。RDS ゲストの特権\[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="30792-108">[Granting Guest Privileges to a Web Server Computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>

- [<span data-ttu-id="30792-109">ビジネス オブジェクトに対してスクリプト作成の安全性を明示する</span><span class="sxs-lookup"><span data-stu-id="30792-109">Marking Business Objects as Safe for Scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)

- [<span data-ttu-id="30792-110">DCOM を使用してビジネス オブジェクトをクライアントに登録する</span><span class="sxs-lookup"><span data-stu-id="30792-110">Registering Business Objects on the Client for Use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)

- [<span data-ttu-id="30792-111">DCOM ストリーム マーシャリング形式を設定する</span><span class="sxs-lookup"><span data-stu-id="30792-111">Setting DCOM Stream Marshaling Format</span></span>](setting-dcom-stream-marshaling-format.md)

- [<span data-ttu-id="30792-112">DCOM で DLL を実行できるようにする</span><span class="sxs-lookup"><span data-stu-id="30792-112">Enabling a DLL to Run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)

- [<span data-ttu-id="30792-113">IIS で仮想サーバーを構成する</span><span class="sxs-lookup"><span data-stu-id="30792-113">Configuring Virtual Servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)

- [<span data-ttu-id="30792-114">IIS でプロセッサごとにスレッドを指定する</span><span class="sxs-lookup"><span data-stu-id="30792-114">Specifying Threads Per Processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)

- [<span data-ttu-id="30792-115">RDS アプリケーションをセキュリティ保護する</span><span class="sxs-lookup"><span data-stu-id="30792-115">Securing RDS Applications</span></span>](securing-rds-applications.md)

- [<span data-ttu-id="30792-116">DataFactory をセーフ モードまたはアクセス制限なしモードで構成する</span><span class="sxs-lookup"><span data-stu-id="30792-116">Configuring DataFactory for Safe or Unrestricted Modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)

- [<span data-ttu-id="30792-117">RDS 関連のテクノロジを使用する (ADO)</span><span class="sxs-lookup"><span data-stu-id="30792-117">Using Related Technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)

- [<span data-ttu-id="30792-118">DataFactory のカスタマイズ (ADO)</span><span class="sxs-lookup"><span data-stu-id="30792-118">DataFactory Customization (ADO)</span></span>](datafactory-customization.md)

- [<span data-ttu-id="30792-119">RDS のトラブルシューティング (ADO)</span><span class="sxs-lookup"><span data-stu-id="30792-119">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)

