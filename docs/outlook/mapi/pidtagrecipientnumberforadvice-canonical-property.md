---
title: PidTagRecipientNumberForAdvice 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 402ef59d4645dd5abaf959188c155902e5bd8eee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594994"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>PidTagRecipientNumberForAdvice 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このプロパティには、メッセージの物理的な配信を通知するために呼び出すメッセージ受信者の電話番号が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE、PR_RECIPIENT_NUMBER_FOR_ADVICE_A、PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|識別子:  <br/> |0x0C14  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、人間の受信者が配信時に存在すると予想されない場合に、電子メールボックスではなく、物理的な宛先への配信と組み合わせて使用することを目的とします。 たとえば、FAX カバー シートの電話番号です。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

