---
title: 取得および複数のプロパティを設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590373"
---
# <a name="getting-and-setting-multiple-properties"></a>取得および複数のプロパティを設定します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
取得するを最小限にできる限り多くのプロパティを設定して、活動を削減したりし、各プロパティに含まれるオーバーヘッドを削減、リモート呼び出しの数です。 サービス ・ プロバイダーがプロパティを取得または変更のためのリモート プロシージャ コールを行う前に収集しようとすると、複数のプロパティを最初に要求することによってこの作業を最適化できます。
  
などの特定のプロパティ セットに属する名前付きのプロパティと、将来の受信者を記述するルーティング リストを使用する場合は、すべての 2 つの呼び出しを使用して受信者を処理します。 受信者のプロパティと、その他の呼び出しの[IMAPIProp::GetProps](imapiprop-getprops.md)にすべての値を取得するためにすべての識別子を取得するために[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を 1 つの呼び出しを使用します。 別に、各受信者について、 **GetProps**への呼び出しの後に**GetIDsFromNames**を呼び出すことは、効率が低下します。 
  

