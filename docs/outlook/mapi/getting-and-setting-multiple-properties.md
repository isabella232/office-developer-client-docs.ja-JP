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
  
最も少ない数の呼び出しで可能な限り多くのプロパティを取得および設定することにより、リモートアクティビティは curtailed で、各プロパティに関連するオーバーヘッドが減少します。 サービスプロバイダーは、取得または変更のためにリモートプロシージャコールを行う前にプロパティの収集を試行しますが、開始するために複数のプロパティを要求することによって、この作業を最適化することができます。
  
たとえば、特定のプロパティセットに属する名前付きプロパティを持つ、今後の受信者について説明するルーティングリストを使用している場合は、すべての受信者を2つの呼び出しで処理します。 1つの呼び出しを[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)に使用して、すべての受信者プロパティの識別子を取得し、その他の[imapiprop:: GetProps](imapiprop-getprops.md)の呼び出しを使用してすべての値を取得します。 別の方法として、 **getidsfromnames**を呼び出して、各受信者の**GetProps**の呼び出しを行う方が、効率が悪くなります。 
  

