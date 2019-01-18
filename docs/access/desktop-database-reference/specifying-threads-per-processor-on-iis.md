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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718183"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="edfb3-102">IIS でのプロセッサごとのスレッドの指定</span><span class="sxs-lookup"><span data-stu-id="edfb3-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="edfb3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="edfb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="edfb3-104">RDS のインターネット情報サービス 4.0 以降を使用している場合は、web サーバー上のレジストリを操作することでプロセッサごとに作成されるスレッドの数を制御できます。</span><span class="sxs-lookup"><span data-stu-id="edfb3-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="edfb3-105">プロセッサごとのスレッド数は、トラフィックが多い場合や、トラフィックが少なくてもクエリのサイズが大きい場合に、パフォーマンスに影響することがあります。</span><span class="sxs-lookup"><span data-stu-id="edfb3-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="edfb3-106">さまざまな状況を試したうえで、最適な設定値を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="edfb3-106">The user should experiment for best results.</span></span>

<span data-ttu-id="edfb3-107">この設定の既定値を決定または変更する方法は、IIS 4.0 サーバーの構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="edfb3-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="edfb3-p102">MDAC 2.1.2.4202.3 (GA) 以降が IIS サーバーにインストールされている場合、RDS では、ASP スクリプトで使用するのと同じコンポーネント サービス (Windows NT では Microsoft Transaction Services) を使用します。プロセッサごとのスレッド数の既定値は 10 です。この既定値を変更するには、サーバー レジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="edfb3-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="edfb3-111">*MaxPoolThreads*は、21、\_の DWORD です。</span><span class="sxs-lookup"><span data-stu-id="edfb3-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="edfb3-112">それは具体的には追加しない限り、 *MaxPoolThreads*は、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="edfb3-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="edfb3-113">有効な値の範囲は、5 から推奨最大値の 20 までです。</span><span class="sxs-lookup"><span data-stu-id="edfb3-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="edfb3-114">レジストリ キーに指定した値が*PoolThreadLimit*キー (同じパスの下にある) の値よりも大きい場合、 *PoolThreadLimit*の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="edfb3-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="edfb3-p104">一方、MDAC 2.1 2.1.1.3711.11 (GA) 以前のバージョンが IIS サーバーにインストールされている場合は、プロセッサごとのスレッド数の既定値は 6 です。既定値を変更するには、IIS サーバーのレジストリに次のキーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="edfb3-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="edfb3-117">*ADCThreads*は、21、\_の DWORD です。</span><span class="sxs-lookup"><span data-stu-id="edfb3-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="edfb3-118">それは具体的には追加しない限り、 *ADCThreads*は、レジストリには表示されません。</span><span class="sxs-lookup"><span data-stu-id="edfb3-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="edfb3-119">有効な値の範囲は、1 から 50 までです。</span><span class="sxs-lookup"><span data-stu-id="edfb3-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="edfb3-120">レジストリ キーで指定した値が 50 より大きい場合は、最大値 (50) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="edfb3-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

