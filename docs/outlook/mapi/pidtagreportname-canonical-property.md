---
title: PidTagReportName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803346"
---
# <a name="pidtagreportname-canonical-property"></a>PidTagReportName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このメッセージのレポートを取得する必要があります受信者の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_REPORT_NAME、PR_REPORT_NAME_A、PR_REPORT_NAME_W  <br/> |
|識別子:  <br/> |0x003A  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

