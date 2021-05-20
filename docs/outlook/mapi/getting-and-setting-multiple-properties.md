---
title: 複数プロパティの取得と設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432262"
---
# <a name="getting-and-setting-multiple-properties"></a>複数プロパティの取得と設定

**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し数が少ないプロパティを可能な限り多く取得して設定すると、リモート アクティビティが抑制され、各プロパティに関連するオーバーヘッドが削減されます。 サービス プロバイダーは、取得または変更のリモート プロシージャ呼び出しを行う前にプロパティを収集しますが、最初に複数のプロパティを要求することで、この作業を最適化できます。
  
たとえば、特定のプロパティ セットに属する名前付きプロパティを持つ将来の受信者を記述するルーティング リストを操作する場合は、2 回の呼び出しですべての受信者を処理します。 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)への 1 つの呼び出しを使用して、すべての受信者プロパティの識別子を取得し、もう一方の呼び出しで[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出してすべての値を取得します。 別の方法として **、GetIDsFromNames** を呼び出し、その後に各受信者の **GetProps** を呼び出す方法は、はるかに効率的です。 
  

