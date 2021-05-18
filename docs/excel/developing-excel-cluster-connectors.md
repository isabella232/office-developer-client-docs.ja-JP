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
# <a name="developing-excel-cluster-connectors"></a>Excel クラスター コネクタの開発

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel クラスター コネクタは、XLL 内のクラスター セーフのユーザー定義関数の呼び出しをクラスター化サーバーに自動的にオフロードする手段を提供します。クラスター セーフのユーザー定義関数の詳細については、「[クラスター セーフ関数](cluster-safe-functions.md)」を参照してください。このオフロードにより、さらに多くのコンピューティング リソースを使用できるようにして、パフォーマンスを向上します。通常、クラスター コネクタは、ハイパフォーマンス コンピューティング クラスター ベンダーによって開発されます。
  
## <a name="cluster-connectors"></a>クラスター コネクタ

クラスター コネクタは定義済みのエントリ ポイントを提供する DLL です。Excel では、このエントリ ポイントを使用して、クラスター セーフなユーザー定義関数の呼び出しを調整します。これは Excel と高性能計算クラスター間のインターフェイスとして、セッションを管理したり、関数呼び出しを実行 (完全修飾の関数名と呼び出しの実引数を渡すことによる) したり、コールバック メカニズムを使用して Excel に呼び出しの結果を返すために使用します。
  
クラスター コネクタを作成するには、DLL を作成して、「[Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)」に記載されているエントリ ポイントを公開します。
  
## <a name="installing-a-cluster-connector"></a>クラスター コネクタのインストール

クラスター コネクタを Excel で使用可能にするには、コネクタのセットアップ コードで、Excel がインストールされているコンピューターにコネクタの DLL をインストールする必要があります。さらに、コネクタのセットアップ コードで、コネクタのエントリを次のレジストリ キーの下に追加する必要もあります。
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
このクラスター コネクタのキーに、次の文字列を指定するノードを追加します。
  
-  `Name`— Excel 内のクラスター コネクタの一覧に表示される名前。
    
-  `Filename`— DLL の完全パス。
    

