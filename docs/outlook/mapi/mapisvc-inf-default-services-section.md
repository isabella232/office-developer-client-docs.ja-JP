---
title: MapiSvc.inf [既定のサービス] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801526"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [既定のサービス] セクション

  
  
**適用されます**: Outlook 
  
**[既定のサービス]** セクションには、すべてのメッセージ サービスの既定値として選択されているメッセージ サービスが一覧表示されます。 これらの既定メッセージ サービスは、 **[サービス]** セクションに記載されているメッセージ サービスのサブセットです。 プロファイルの構成プログラムは、既定のプロファイルを作成する場合、このセクションのメッセージ サービスは、自動的に含まれています。 
  
エントリに示すように次のよう、 **[サービス]** セクションのエントリとして同じ形式を使用します。 
  
 **[既定のサービス]**
  
 _メッセージ サービス セクション名_ =  _メッセージ サービス名_
  
次のエントリは、mapisvc.inf の前の図に示すように **[サービスの既定値]** セクションに含まれます。 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


