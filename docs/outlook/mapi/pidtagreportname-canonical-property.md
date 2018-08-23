---
title: PidTagReportName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569583"
---
# <a name="pidtagreportname-canonical-property"></a>PidTagReportName 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
このメッセージのレポートを取得する必要があります受信者の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W  <br/> |
|識別子:  <br/> |0x003A  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、このメッセージに対して生成されたすべてのレポートを受信する送信者を委任した受信者のアドレスのプロパティの例を示します。
  
レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこれらのプロパティを設定する必要があります。 設定されていない場合、レポートは、メッセージの送信者に送信されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

