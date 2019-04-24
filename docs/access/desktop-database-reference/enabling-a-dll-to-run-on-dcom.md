---
title: DCOM で実行する DLL の有効化
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b97f4e8050cf293621c7b7fc79437c89171d86fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293547"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a><span data-ttu-id="880de-102">DCOM で実行する DLL の有効化</span><span class="sxs-lookup"><span data-stu-id="880de-102">Enabling a DLL to run on DCOM</span></span>


<span data-ttu-id="880de-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="880de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="880de-104">次の手順では、ビジネスオブジェクトのダイナミックリンクライブラリで、コンポーネントサービス経由で DCOM と Microsoft インターネットインフォメーションサービス (HTTP) の両方を使用できるようにする方法の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="880de-104">The following steps outline how to enable a business object dynamic-link libraries to use both DCOM and Microsoft Internet Information Services (HTTP) via Component Services.</span></span>

1.  <span data-ttu-id="880de-p101">コンポーネント サービス MMC スナップインに新しい空のパッケージを作成します。 コンポーネント サービス MMC スナップインを使ってパッケージを作成し、このパッケージに DLL を追加します。これにより、DCOM を介して .dll にアクセスできるようになりますが、IIS を介したアクセスはできなくなります (.dll のレジストリを確認すると、 **Inproc** キーが空になっているのがわかります。後で説明するようにアクティブ化属性を設定すると、 **Inproc** キーに値が追加されます)。</span><span class="sxs-lookup"><span data-stu-id="880de-p101">Create a new empty package in the Component Services MMC snap-in. You will use the Component Services MMC snap-in to create a package and add the DLL into this package. This makes the .dll accessible through DCOM, but it removes the accessibility through IIS. (If you check in the registry for the .dll, the **Inproc** key is now empty; setting the Activation attribute, explained later in this topic, adds a value in the **Inproc** key.)</span></span>

2.  <span data-ttu-id="880de-p102">パッケージにビジネス オブジェクトをインストールします。 または[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトをパッケージにインポートします。</span><span class="sxs-lookup"><span data-stu-id="880de-p102">Install a business object into the package. -or- Import the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object into the package.</span></span>

3.  <span data-ttu-id="880de-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span><span class="sxs-lookup"><span data-stu-id="880de-p103">Set the Activation attribute for the package to **In the creator's process** (Library application). To make the .dll accessible through DCOM and IIS on the same computer, you must set the component's Activation attribute in the Component Services MMC snap-in. After you set the attribute to **In the creator's process**, you will notice that an **Inproc** server key in the registry has been added that points to a Component Services surrogate .dll.</span></span>

