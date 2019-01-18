---
title: DataFactory をセーフ モードまたはアクセス制限なしモードで構成する
TOCTitle: Configuring DataFactory for Safe or Unrestricted Modes
ms:assetid: 1516068f-1b02-3236-f6a9-9fdeff098e52
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248915(v=office.15)
ms:contentKeyID: 48543400
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4313d48359499eaf249a68eb97408c8ed4ecb88
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702734"
---
# <a name="configuring-datafactory-for-safe-or-unrestricted-modes"></a><span data-ttu-id="a848d-102">DataFactory をセーフ モードまたはアクセス制限なしモードで構成する</span><span class="sxs-lookup"><span data-stu-id="a848d-102">Configuring DataFactory for Safe or Unrestricted Modes</span></span>


<span data-ttu-id="a848d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a848d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a848d-p101">既定では、ADO は "安全な" [RDSServer.DataFactory](datafactory-object-rdsserver.md) 構成でインストールされます。RDS Server コンポーネントのセーフ モードの条件は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a848d-p101">By default, ADO is installed with a "safe" [RDSServer.DataFactory](datafactory-object-rdsserver.md) configuration. Safe mode for RDS Server components means that the following are true:</span></span>

1.  <span data-ttu-id="a848d-106">RDSServer.DataFactory にハンドラーが必須である (必須かどうかは、レジストリ キーの設定によって決まります)。</span><span class="sxs-lookup"><span data-stu-id="a848d-106">Handler is required with the RDSServer.DataFactory (this is mandated by a registry key setting).</span></span>

2.  <span data-ttu-id="a848d-107">既定のハンドラーである msdfmap.handler が登録され、安全なハンドラーの一覧にあり、既定のハンドラーとしてマークされている。</span><span class="sxs-lookup"><span data-stu-id="a848d-107">The default handler, msdfmap.handler, is registered, present in the safe-handler list, and marked as the default handler.</span></span>

3.  <span data-ttu-id="a848d-p102">Windows ディレクトリに msdfmap.ini ファイルがインストールされている。3 層モードで RDS を使用する場合は、必要に応じてこのファイルを事前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a848d-p102">Msdfmap.ini file is installed in the Windows directory. You must configure this file according to your needs, before using RDS in three-tier mode.</span></span>

<span data-ttu-id="a848d-110">または、アクセス制限なしの **DataFactory** インストールを構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a848d-110">Optionally, you can configure an unrestricted **DataFactory** installation.</span></span> <span data-ttu-id="a848d-111">**DataFactory** は、カスタム ハンドラーがなくても直接使用できます。</span><span class="sxs-lookup"><span data-stu-id="a848d-111">**DataFactory** can be used directly without the custom handler.</span></span> <span data-ttu-id="a848d-112">接続文字列を変更してカスタム ハンドラーを使うことができますが、そうする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a848d-112">Users can still use a custom handler by modifying the connection strings, but it is not required.</span></span> <span data-ttu-id="a848d-113">**RDSServer.DataFactory**オブジェクトを使用する場合の影響の詳細については、 [RDS アプリケーションをセキュリティで保護する](securing-rds-applications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a848d-113">For more information about the implications of using the **RDSServer.DataFactory** object, see [Securing RDS Applications](securing-rds-applications.md).</span></span>

<span data-ttu-id="a848d-p104">安全に構成を行うために、レジストリ ファイル handsafe.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。セーフ モードで実行するには、handsafe.reg を実行します。アクセス制限なしの構成を行うためには、レジストリ ファイル handunsf.reg がハンドラー レジストリ エントリのセットアップ用に用意されています。アクセス制限なしモードで実行するには、handunsf.reg を実行します。</span><span class="sxs-lookup"><span data-stu-id="a848d-p104">The registry file handsafe.reg has been provided to set up the handler registry entries for a safe configuration. To run in safe mode, run handsafe.reg. The registry file handunsf.reg has been provided to set up the handler registry entries for an unrestricted configuration. To run in unrestricted mode, run handunsf.reg.</span></span>

<span data-ttu-id="a848d-117">Handsafe.reg または handunsf.reg というのいずれかを実行すると、停止して web サーバー上の World Wide Web 発行サービスを再起動するには、コマンド ウィンドウで次のコマンドを入力:「NET W3SVC を停止」と「ネット スタート W3SVC」です。</span><span class="sxs-lookup"><span data-stu-id="a848d-117">After running either handsafe.reg or handunsf.reg, you must stop and restart the World Wide Web Publishing Service on the web server by typing the following commands in a command window: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

<span data-ttu-id="a848d-118">RDS のカスタム ハンドラー機能の使用方法の詳細については、技術記事「Using the Customization Handler Feature in RDS 2.1」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a848d-118">For more information about using the customization handler feature of RDS, see the technical article Using the Customization Handler Feature in RDS 2.1.</span></span>

