---
title: PidTagAdditionalRenEntryIds の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802422"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>PidTagAdditionalRenEntryIds の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
エントリ特定の特殊フォルダーの Id にはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|識別子:  <br/> |0x36D8  <br/> |
|データを入力します。  <br/> |PT_MV_BINARY  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>備考

この複数値を持つプロパティの最初の 5 つのエントリは、ストア内に存在する場合に、次の特別なフォルダーに適用されます。
  
0 - [競合] フォルダー
  
1-同期の失敗フォルダー
  
2-ローカルの失敗フォルダー
  
3-サーバーの失敗] フォルダー
  
4-迷惑メール フォルダー
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
[[MS OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> 識別し、だまして受信者 (パスワードやその他の個人情報) などの機密情報を盗み、以外の信頼できる発行元に設計された電子メール メッセージをマークします。
    
[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)


[ストア API について](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

