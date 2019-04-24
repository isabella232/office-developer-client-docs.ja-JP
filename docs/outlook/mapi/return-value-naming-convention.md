---
title: 戻り値の名前付け規則
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279826"
---
# <a name="return-value-naming-convention"></a>戻り値の名前付け規則

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPICODE。H ヘッダーファイルには、クライアントまたはサービスプロバイダーがインターフェイスメソッドの実装から返す可能性のある多くの値が含まれているか、呼び出しから返される可能性があります。
  
警告とエラーの条件を表すコードは、プレフィックス MAPI、アンダースコア、およびコードの種類を示す W または E のいずれかで始まる、異なる名前付け規則に従います。 コードの残りの部分は、条件を記述する短い文字列です。 文字列内の各単語は、アンダースコアで区切られています。 たとえば、エラー値 MAPI_E_TOO_COMPLEX は、呼び出しで要求された内容を実装が処理できなかったことを示します。 警告値 MAPI_W_PARTIAL_COMPLETION は、呼び出しが成功したが、問題が発生したことを示します。 操作の一部のみが正常に完了しました。
  

