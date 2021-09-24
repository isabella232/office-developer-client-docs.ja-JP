---
title: よく使うプロパティの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 66dc993df65a12e0e3bc9ff22b043ba0e97b8471
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550142"
---
# <a name="saving-frequently-used-properties"></a>よく使うプロパティの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
取得に時間とリソースを要し、頻繁にアクセスするデータを格納することで、パフォーマンスを向上させます。 余分なメモリを使用すると、取得を繰り返す方が良いオプションになる場合があります。 このデータを格納するためのキャッシュを作成する場合は、注意と注意が必要です。 キャッシュの設計が不十分な場合、パフォーマンスに悪影響を及ぼす可能性があります。
  
たとえば、ほとんどの対人間メッセージ (IPM) クライアントは、一般的なセッション中に何度もフォルダーの IPM サブツリーを表示および開く必要があります。 これらの各フォルダーのエントリ識別子を格納することで、パフォーマンスを向上させることができます。 
  

