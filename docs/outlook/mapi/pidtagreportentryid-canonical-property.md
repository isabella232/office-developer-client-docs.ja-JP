---
title: PidTagReportEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803338"
---
# <a name="pidtagreportentryid-canonical-property"></a>PidTagReportEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このメッセージのレポートを受信する受信者のエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_REPORT_ENTRYID  <br/> |
|識別子:  <br/> |0x0045  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI の封筒  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、送信者がこのメッセージに対して生成されたすべてのレポートを受信するのには、委任した受信者のアドレスのプロパティのいずれかです。
  
レポートを別のユーザーにルーティングする必要がありますクライアント アプリケーションは、メッセージの送信時にこのプロパティを設定する必要があります。 設定されていない場合、レポートは、メッセージの送信者に送信されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
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
