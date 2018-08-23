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
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800166"
---
# <a name="getting-and-setting-multiple-properties"></a>取得および複数のプロパティを設定します。

**適用対象**: Outlook 
  
取得するを最小限にできる限り多くのプロパティを設定して、活動を削減したりし、各プロパティに含まれるオーバーヘッドを削減、リモート呼び出しの数です。 サービス ・ プロバイダーがプロパティを取得または変更のためのリモート プロシージャ コールを行う前に収集しようとすると、複数のプロパティを最初に要求することによってこの作業を最適化できます。
  
などの特定のプロパティ セットに属する名前付きのプロパティと、将来の受信者を記述するルーティング リストを使用する場合は、すべての 2 つの呼び出しを使用して受信者を処理します。 受信者のプロパティと、その他の呼び出しの[IMAPIProp::GetProps](imapiprop-getprops.md)にすべての値を取得するためにすべての識別子を取得するために[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を 1 つの呼び出しを使用します。 別に、各受信者について、 **GetProps**への呼び出しの後に**GetIDsFromNames**を呼び出すことは、効率が低下します。 
  

