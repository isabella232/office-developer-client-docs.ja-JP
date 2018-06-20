---
title: PidLidAutoProcessState の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801822"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>PidLidAutoProcessState の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
電子メール メッセージの自動処理で使用されるオプションを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidSniffState  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x0000851A  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

プロパティは"0x00000000"の既定値を使用する場合に入力が失われている可能性があります。 設定するとこのプロパティに次の表の値のいずれかに設定します。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |メッセージを自動的に処理しません。  <br/> |
|0x00000001  <br/> |メッセージを自動的に処理するか、メッセージを開いたとき。  <br/> |
|0x00000002  <br/> |メッセージを開いたときにのみメッセージを処理します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

