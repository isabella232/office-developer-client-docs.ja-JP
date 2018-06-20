---
title: PidTagMessageSize の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802996"
---
# <a name="pidtagmessagesize-canonical-property"></a>PidTagMessageSize の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ オブジェクトのすべてのプロパティのサイズの合計 (バイト単位) にはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MESSAGE_SIZE  <br/> |
|識別子:  <br/> |0x0E08  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

メッセージ オブジェクトがこのプロパティを公開することをお勧めします。 メッセージのサイズは、メッセージが別の 1 つのメッセージ ・ ストアに移動した場合に転送されるバイトのおおよその数を示します。 メッセージ オブジェクトのすべてのプロパティのサイズの合計である、多くのメッセージのテキストだけよりもかなり大きいです。 
  
ほとんどのメッセージは、プロバイダーの計算、処理されるメッセージに対してこのプロパティを格納します。 ただし、いくつかのメッセージ ストア プロバイダーはこのプロパティをサポートしていません。 どのような場合は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)または[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドが呼び出されるまでこのプロパティは使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージのストア オブジェクトの許可された操作を指定します。
    
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

