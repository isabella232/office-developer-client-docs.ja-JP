---
title: XML レコードセットを保存するシナリオ
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 378d3b1fc559cc07c1eb3a58621a8a4bd09a06ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861827"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="71888-102">XML レコードセットの永続化シナリオ</span><span class="sxs-lookup"><span data-stu-id="71888-102">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="71888-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="71888-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="71888-104">XML レコードセットの永続化シナリオ</span><span class="sxs-lookup"><span data-stu-id="71888-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="71888-105">このシナリオでは、 **Response** オブジェクトの内容を Active Server Pages (ASP) の **Response** オブジェクトに直接保存する ASP アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="71888-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="71888-106">[!メモ] このシナリオを作成するには、サーバーに Internet Information Server 5.0 (IIS) 以降がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="71888-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="71888-107">返される **Recordset** は、 [RDS.DataControl](datacontrol-object-rds.md) を使用して Internet Explorer に表示されます。</span><span class="sxs-lookup"><span data-stu-id="71888-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="71888-108">このシナリオを作成するために必要な手順は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71888-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="71888-109">アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="71888-109">Set up the application.</span></span>

2.  <span data-ttu-id="71888-110">データを取得します。</span><span class="sxs-lookup"><span data-stu-id="71888-110">Get the data.</span></span>

3.  <span data-ttu-id="71888-111">データを送信します。</span><span class="sxs-lookup"><span data-stu-id="71888-111">Send the data.</span></span>

4.  <span data-ttu-id="71888-112">データを受信し、表示します。</span><span class="sxs-lookup"><span data-stu-id="71888-112">Receive and display the data.</span></span>

### <a name="next-step"></a><span data-ttu-id="71888-113">次のステップ</span><span class="sxs-lookup"><span data-stu-id="71888-113">Next step</span></span>

[<span data-ttu-id="71888-114">手順 1: アプリケーションを設定する</span><span class="sxs-lookup"><span data-stu-id="71888-114">Step 1: Set Up the Application</span></span>](step-1-set-up-the-application.md)

