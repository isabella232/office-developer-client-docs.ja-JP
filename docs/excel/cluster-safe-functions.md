---
title: クラスター セーフ関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 787badaf-8782-454d-a016-7eae83bbd8a9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f73f49e4d76a8545399eede283b70551ee6569f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798760"
---
# <a name="cluster-safe-functions"></a><span data-ttu-id="d4f77-103">クラスター セーフ関数</span><span class="sxs-lookup"><span data-stu-id="d4f77-103">Cluster Safe Functions</span></span>

<span data-ttu-id="d4f77-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4f77-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d4f77-p101">Excel 2013 では、Excel が専用のクラスター コネクタ インタ フェースを介して、高パフォーマンスのコンピューティング クラスターに対するユーザー定義関数 (UDF) 呼び出しをオフロードできます。計算クラスターのベンダーによりクラスター コネクタが提供されています。UDF の作成者は、作成する UDF をクラスター セーフとして宣言できます。クラスター コネクタが存在する場合、Excel はこれらの UDF の呼び出しをオフロードするためにクラスター コネクタに送信します。</span><span class="sxs-lookup"><span data-stu-id="d4f77-p101">In Excel 2013, Excel can offload User-Defined Function (UDF) calls to a high-performance computing cluster through a dedicated cluster connector interface. Compute cluster vendors provide Cluster Connectors. UDF authors can declare their UDFs as cluster safe and then, when a cluster connector is present, Excel sends calls to these UDFs to the cluster connector for offloading.</span></span>
  
<span data-ttu-id="d4f77-p102">Excel は、再計算中にクラスター セーフ UDF を検出すると、現在実行中の XLL 名、クラスター セーフ UDF、および任意のパラメーターをクラスター コネクタに渡します。コネクタは UDF 呼び出しをリモートで実行し、結果を Excel に返します。依存しない計算が続行され、クラスター コネクタは UDF の実行を完了すると結果を Excel に渡して、依存する計算を続行します。この非同期動作のメカニズムは、非同期の動作を管理するのが UDF 作成者ではなくクラスター コネクタであるという点を除けば、非同期 UDF によって使用されるメカニズムと同じです。通常、クラスター コネクタは XLL shim を実装して XLL を読み込み、計算クラスター ノード上で UDF を実行します。</span><span class="sxs-lookup"><span data-stu-id="d4f77-p102">When Excel discovers a cluster-safe UDF during recalculation, it passes the name of the XLL that is currently running, the name of the cluster-safe UDF, and any parameters to the cluster connector. The connector runs the UDF call remotely and returns the results to Excel. Non-dependent calculation continues and when the cluster connector has finished running the UDF, it passes the results to Excel and dependent calculations continue. The mechanism for this asynchronous behavior mimics the mechanism used by asynchronous UDFs, except that the cluster connector manages the asynchronous aspects instead of the UDF author. Typically, a cluster connector implements an XLL shim to load XLLs and run UDFs on compute cluster nodes.</span></span>
  
<span data-ttu-id="d4f77-p103">クラスター セーフとして UDF を宣言するしくみは、マルチ スレッドの再計算に関して UDF を安全として宣言するしくみに似ています。ただし、UDF は必ずしも同じ Excel セッションの他の UDF と同じコンピューター上で実行されるわけではないため、クラスター セーフ UDF を記述する際には、さまざまな考慮事項が存在します。</span><span class="sxs-lookup"><span data-stu-id="d4f77-p103">The mechanics of declaring UDFs as cluster-safe resemble those of declaring UDFs as safe for multi-threaded recalculation. However, because the UDF is not necessarily running on the same computer as other UDFs from the same Excel session, there are different considerations when writing cluster-safe UDFs.</span></span>
  
<span data-ttu-id="d4f77-115">UDF をクラスター セーフとして登録するには、**Excel12** または **Excel12v** インターフェイスから [xlfRegister (形式 1)](xlfregister-form-1.md) コールバック関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4f77-115">To register a UDF as cluster-safe, you must call the [xlfRegister (Form 1)](xlfregister-form-1.md) callback function through the **Excel12** or **Excel12v** interface. For more information about these interfaces, see the Excel4/Excel12 and Excel4v/Excel12v. Registering a UDF as cluster-safe through the Excel4 or Excel4v interface is not supported.</span></span> <span data-ttu-id="d4f77-116">これらのインターフェイスの詳細については、「[Excel4/Excel12](excel4-excel12.md)」と「[Excel4v/Excel12v](excel4v-excel12v.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4f77-116">For more information about these interfaces, see the [Excel4/Excel12](excel4-excel12.md) and [Excel4v/Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="d4f77-117">**Excel4** または **Excel4v** インターフェイスを介して UDF をクラスター セーフとして登録することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d4f77-117">Registering a UDF as cluster-safe through the **Excel4** or **Excel4v** interface is not supported.</span></span> 
  
<span data-ttu-id="d4f77-p105">クラスター セーフとして関数を登録する場合は、関数がクラスター セーフな方法で動作することを確認する必要があります。クラスター コネクタの厳密な動作は実装によって異なりますが、UDF は、分散コンピューター システム上で実行し、また次のような特徴を持つように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4f77-p105">If you register a function as cluster-safe, you must ensure that the function behaves in a cluster-safe way. Although the exact behavior of the cluster connector is implementation-specific, you should design your UDF to run on a distributed computer system and to have the following characteristics:</span></span>
  
- <span data-ttu-id="d4f77-p106">UDF はメモリの状態に依存しない。たとえば、UDF は既存のメモリ内キャッシュなどに依存していてはなりません。</span><span class="sxs-lookup"><span data-stu-id="d4f77-p106">A UDF should not rely on any memory state. For example, a UDF should not rely on an existing in-memory cache.</span></span>
    
- <span data-ttu-id="d4f77-122">UDF はクラスター コネクタ プロバイダーでサポートされていない Excel コールバックを実行しない。</span><span class="sxs-lookup"><span data-stu-id="d4f77-122">A UDF should not perform Excel callbacks that the cluster connector provider does not support.</span></span>
    
<span data-ttu-id="d4f77-123">クラスター セーフ UDF には、クラスター セーフの動作の他にも、次のような技術的な制限があります。</span><span class="sxs-lookup"><span data-stu-id="d4f77-123">In addition to cluster-safe behavior, there are the following technical restrictions on cluster-safe UDFs:</span></span>
  
1. <span data-ttu-id="d4f77-124">XLOPER 引数 ('P' 型、'R' 型) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="d4f77-124">No XLOPER arguments (types 'P', 'R').</span></span>
    
2. <span data-ttu-id="d4f77-125">範囲参照をサポートする XLOPER12 引数 ('U' 型) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="d4f77-125">No XLOPER12 arguments that support range references (type 'U').</span></span>
    
3. <span data-ttu-id="d4f77-126">マクロ シートの同等の関数であってはなりません ('#' と '&amp;' を組み合わせることはできません)。</span><span class="sxs-lookup"><span data-stu-id="d4f77-126">Cannot be a macro sheet equivalent function ('#' and '&amp;' cannot be combined).</span></span>
    
<span data-ttu-id="d4f77-127">実行時間が短い UDF の場合は、オフロードのオーバーヘッドが UDFの実行にかかる時間よりも大きくなって、このインフラストラクチャを使用してもほとんどプラスにならない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d4f77-127">For UDFs with shorter execution times, the overhead of offloading may be larger than the time it takes the UDF to execute, negating many of the benefits of using this infrastructure.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d4f77-128">クラスター セーフ UDF は非同期 UDF として宣言できません。</span><span class="sxs-lookup"><span data-stu-id="d4f77-128">You cannot declare a cluster-safe UDF as an asynchronous UDF.</span></span> 
  
<span data-ttu-id="d4f77-129">UDF は、[xlRunningOnCluster](xlrunningoncluster.md) コールバック関数を呼び出すことによって、クラスター コネクタを使用して実行されているかどうかを判別できます。</span><span class="sxs-lookup"><span data-stu-id="d4f77-129">A UDF can determine whether it is being run using a cluster connector by calling the [xlRunningOnCluster](xlrunningoncluster.md) callback function.</span></span> 
  

