---
title: IIS でプロセッサごとにスレッドを指定する
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476794"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="e30f0-102">IIS でプロセッサごとにスレッドを指定する</span><span class="sxs-lookup"><span data-stu-id="e30f0-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="e30f0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e30f0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e30f0-p101">Internet Information Services 4.0 以降で RDS を使用する場合は、Web サーバーのレジストリを操作することによって、プロセッサごとに作成されるスレッドの数を制御できます。プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。さまざまな状況を試したうえで、最適な設定値を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e30f0-p101">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server. The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes. The user should experiment for best results.</span></span>

<span data-ttu-id="e30f0-107">この設定の既定値を決定または変更する方法は、IIS 4.0 サーバーの構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e30f0-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="e30f0-p102">MDAC 2.1.2.4202.3 (GA) 以降が IIS サーバーにインストールされている場合、RDS では、ASP スクリプトで使用するのと同じコンポーネント サービス (Windows NT では Microsoft Transaction Services) を使用します。プロセッサごとのスレッド数の既定値は 10 です。この既定値を変更するには、サーバー レジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e30f0-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="e30f0-111">*MaxPoolThreads*は、21、\_の DWORD です。</span><span class="sxs-lookup"><span data-stu-id="e30f0-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e30f0-112">それは具体的には追加しない限り、 *MaxPoolThreads*は、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="e30f0-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e30f0-113">有効な値の範囲は、5 から推奨最大値の 20 までです。</span><span class="sxs-lookup"><span data-stu-id="e30f0-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="e30f0-114">レジストリ キーに指定した値が*PoolThreadLimit*キー (同じパスの下にある) の値よりも大きい場合、 *PoolThreadLimit*の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e30f0-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="e30f0-p104">一方、MDAC 2.1 2.1.1.3711.11 (GA) 以前のバージョンが IIS サーバーにインストールされている場合は、プロセッサごとのスレッド数の既定値は 6 です。既定値を変更するには、IIS サーバーのレジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e30f0-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="e30f0-117">*ADCThreads*は、21、\_の DWORD です。</span><span class="sxs-lookup"><span data-stu-id="e30f0-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e30f0-118">それは具体的には追加しない限り、 *ADCThreads*は、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="e30f0-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e30f0-119">有効な値の範囲は、1 から 50 までです。</span><span class="sxs-lookup"><span data-stu-id="e30f0-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="e30f0-120">レジストリ キーで指定した値が 50 より大きい場合は、最大値 (50) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e30f0-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

