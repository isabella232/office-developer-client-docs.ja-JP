---
title: IIS でのプロセッサごとのスレッドの指定
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308590"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="8e3d9-102">IIS でのプロセッサごとのスレッドの指定</span><span class="sxs-lookup"><span data-stu-id="8e3d9-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="8e3d9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e3d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e3d9-104">インターネットインフォメーションサービス4.0 以降で RDS を使用する場合、web サーバー上のレジストリを操作することによって、プロセッサごとに作成されるスレッドの数を制御できます。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="8e3d9-105">プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="8e3d9-106">さまざまな状況を試したうえで、最適な設定値を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-106">The user should experiment for best results.</span></span>

<span data-ttu-id="8e3d9-107">この設定の既定値を決定または変更する方法は、IIS 4.0 サーバーの構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="8e3d9-p102">MDAC 2.1.2.4202.3 (GA) 以降が IIS サーバーにインストールされている場合、RDS では、ASP スクリプトで使用するのと同じコンポーネント サービス (Windows NT では Microsoft Transaction Services) を使用します。プロセッサごとのスレッド数の既定値は 10 です。この既定値を変更するには、サーバー レジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="8e3d9-111">ここで、 *maxpoolthreads*は\_REG DWORD です。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="8e3d9-112">*MaxPoolThreads* は、指定して追加しない限り、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="8e3d9-113">有効な値の範囲は、5 から推奨最大値の 20 までです。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="8e3d9-114">レジストリ キーで指定した値が *PoolThreadLimit* キー (同じパスにあります) の値より大きい場合、*PoolThreadLimit* の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="8e3d9-p104">一方、MDAC 2.1 2.1.1.3711.11 (GA) 以前のバージョンが IIS サーバーにインストールされている場合は、プロセッサごとのスレッド数の既定値は 6 です。既定値を変更するには、IIS サーバーのレジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="8e3d9-117">ここで、 *adcthreads*は\_REG DWORD です。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="8e3d9-118">*ADCThreads* は、指定して追加しない限り、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="8e3d9-119">有効な値の範囲は、1 から 50 までです。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="8e3d9-120">レジストリ キーで指定した値が 50 より大きい場合は、最大値 (50) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e3d9-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

