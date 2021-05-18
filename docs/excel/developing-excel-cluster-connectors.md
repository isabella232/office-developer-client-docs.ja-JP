---
title: Excel クラスター コネクタの開発
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412598"
---
# <a name="developing-excel-cluster-connectors"></a><span data-ttu-id="c3c06-103">Excel クラスター コネクタの開発</span><span class="sxs-lookup"><span data-stu-id="c3c06-103">Developing Excel Cluster Connectors</span></span>

<span data-ttu-id="c3c06-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c3c06-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c3c06-p101">Excel クラスター コネクタは、XLL 内のクラスター セーフのユーザー定義関数の呼び出しをクラスター化サーバーに自動的にオフロードする手段を提供します。クラスター セーフのユーザー定義関数の詳細については、「[クラスター セーフ関数](cluster-safe-functions.md)」を参照してください。このオフロードにより、さらに多くのコンピューティング リソースを使用できるようにして、パフォーマンスを向上します。通常、クラスター コネクタは、ハイパフォーマンス コンピューティング クラスター ベンダーによって開発されます。</span><span class="sxs-lookup"><span data-stu-id="c3c06-p101">Excel cluster connectors provide a means for automatically offloading cluster-safe user-defined function calls in an XLL to a clustered server. For a description of cluster-safe user-defined functions, see [Cluster Safe Functions](cluster-safe-functions.md). This offloading can improve performance by enabling more computing resources to be used. A cluster connector is typically developed by a high performance compute cluster vendor.</span></span>
  
## <a name="cluster-connectors"></a><span data-ttu-id="c3c06-109">クラスター コネクタ</span><span class="sxs-lookup"><span data-stu-id="c3c06-109">Cluster Connectors</span></span>

<span data-ttu-id="c3c06-p102">クラスター コネクタは定義済みのエントリ ポイントを提供する DLL です。Excel では、このエントリ ポイントを使用して、クラスター セーフなユーザー定義関数の呼び出しを調整します。これは Excel と高性能計算クラスター間のインターフェイスとして、セッションを管理したり、関数呼び出しを実行 (完全修飾の関数名と呼び出しの実引数を渡すことによる) したり、コールバック メカニズムを使用して Excel に呼び出しの結果を返すために使用します。</span><span class="sxs-lookup"><span data-stu-id="c3c06-p102">A cluster connector is a DLL that provides defined entry points that Excel uses to coordinate cluster-safe user-defined function calls. It serves as an interface between Excel and the high-performance compute cluster, for session management, for making function calls (by passing the fully-qualified function name and the call's actual arguments), and for returning call results to Excel through a callback mechanism.</span></span>
  
<span data-ttu-id="c3c06-112">クラスター コネクタを作成するには、DLL を作成して、「[Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)」に記載されているエントリ ポイントを公開します。</span><span class="sxs-lookup"><span data-stu-id="c3c06-112">To create a cluster connector, create a DLL that exposes the entry points listed in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md).</span></span>
  
## <a name="installing-a-cluster-connector"></a><span data-ttu-id="c3c06-113">クラスター コネクタのインストール</span><span class="sxs-lookup"><span data-stu-id="c3c06-113">Installing a Cluster Connector</span></span>

<span data-ttu-id="c3c06-p103">クラスター コネクタを Excel で使用可能にするには、コネクタのセットアップ コードで、Excel がインストールされているコンピューターにコネクタの DLL をインストールする必要があります。さらに、コネクタのセットアップ コードで、コネクタのエントリを次のレジストリ キーの下に追加する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c3c06-p103">To make a cluster connector available in Excel, the setup code of the connector must install the DLL of the connector on the computer where Excel is installed. In addition, the setup code of the connector must add an entry for the connector under the following registry key:</span></span>
  
<span data-ttu-id="c3c06-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="c3c06-116">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors</span></span>\
  
<span data-ttu-id="c3c06-117">このクラスター コネクタのキーに、次の文字列を指定するノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c3c06-117">Add a node to this key for the cluster connector that specifies the following strings:</span></span>
  
-  <span data-ttu-id="c3c06-118">`Name`— Excel 内のクラスター コネクタの一覧に表示される名前。</span><span class="sxs-lookup"><span data-stu-id="c3c06-118">`Name`—the name that will appear in the list of cluster connectors in Excel.</span></span>
    
-  <span data-ttu-id="c3c06-119">`Filename`— DLL の完全パス。</span><span class="sxs-lookup"><span data-stu-id="c3c06-119">`Filename`—the full path for the DLL.</span></span>
    

