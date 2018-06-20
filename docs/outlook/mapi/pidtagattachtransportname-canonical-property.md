---
title: PidTagAttachTransportName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802507"
---
# <a name="pidtagattachtransportname-canonical-property"></a>PidTagAttachTransportName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
TNEF メッセージに関連付けられるように変更された添付ファイルの名前が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_TRANSPORT_NAME、PR_ATTACH_TRANSPORT_NAME_A、PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|識別子:  <br/> |0x370C  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

TNEF およびトランスポート プロバイダーは、これらのプロパティを使用します。 通常クライアント アプリケーションで使用します。 
  
これらのプロパティは、基になるメッセージング システムでは、指定されたファイル名をサポートしていない場合、TNEF で通常使用されます。 などのユーザー設定を名前付きの 5 つのファイルなど、同じ名前の複数のファイルを添付するときに使用します。SYS です。 トランスポート プロバイダーは、一意であるかどうかを確認するのには名前を変更しなければなりません。 各変更後の名前は、その添付ファイルの**PR_ATTACH_TRANSPORT_NAME**および関連付けられたプロパティに表示されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

