---
title: Excel クラスター コネクタ関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798800"
---
# <a name="excel-cluster-connector-functions"></a>Excel クラスター コネクタ関数

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 クラスター コネクタ DLL は、このセクションで取り上げる関数を実装する必要があります。
  
このセクションの参照トピックで言及されている戻り値は、SDK インクルード ファイル (xlcall.h) で定義されています。
  
## <a name="cluster-connector-architecture"></a>クラスター コネクタのアーキテクチャ

Excel は、クラスター コネクタのエントリ ポイントを呼び出して、ユーザー定義関数呼び出しを高パフォーマンスのコンピューティング クラスターに転送し、クラスター セッション管理を行います。
  
## <a name="in-this-section"></a>このセクションの内容

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>関連項目



[Excel クラスター コネクタの開発](developing-excel-cluster-connectors.md)
  
[クラスター セーフ関数](cluster-safe-functions.md)

