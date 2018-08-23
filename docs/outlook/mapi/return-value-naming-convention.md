---
title: 戻り値の名前付け規則
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581847"
---
# <a name="return-value-naming-convention"></a>戻り値の名前付け規則

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPICODE。H ヘッダー ファイルには、多くのクライアントまたはサービス プロバイダーはインターフェイス メソッドの実装から返すことがありますか、呼び出しから返される可能性があります参照してください値が含まれています。
  
警告とエラーの状態を表すためのコードは、MAPI のプレフィックス、アンダー スコア、および W またはコードの種類を示すために E で始まる別の名前付け規則に従います。 コードの残りの部分は、条件を記述する短い文字列です。 文字列内の各単語は、アンダー スコアで区切られます。 たとえば、エラー値 MAPI_E_TOO_COMPLEX は、その実装に処理できませんでした呼び出しで要求されたどのようなを示します。 警告値 MAPI_W_PARTIAL_COMPLETION は、呼び出しが成功したことが、問題が発生したことを示します。 操作の一部だけが正常に完了しました。
  

