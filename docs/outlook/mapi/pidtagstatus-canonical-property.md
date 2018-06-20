---
title: PidTagStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01a65306e5e0d34ed6f1ce7231227224868ff5cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803585"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーの状態を定義するフラグのビットマスクで、32 ビットが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_STATUS  <br/> |
|識別子:  <br/> |0x360B  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

フォルダーに対してこのプロパティは、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティに似ています。 そのフラグは、クライアント アプリケーションのみに提供され、メッセージ ・ ストアには影響しません。 クライアントでは、使用したり、これらの設定を無視することができます。 クライアントでは、このプロパティのクライアントが定義可能なビットの値も定義できます。
  
1 つ以上次のフラグのビットマスクを設定できます。
  
FLDSTATUS_DELMARKED 
  
> フォルダーが削除対象としてマークします。 クライアント アプリケーションでは、このフラグを設定します。
    
FLDSTATUS_HIDDEN 
  
> フォルダーが非表示にします。
    
FLDSTATUS_HIGHLIGHTED 
  
> フォルダーがハイライトされます、たとえば、ビデオの逆の順序で表示されています。
    
FLDSTATUS_TAGGED 
  
> フォルダーがタグ付けされます。
    
メッセージ ストア プロバイダーは、このプロパティを設定する 1 つのフォルダーにまたは、アプリケーションに適切な状態を解釈のこれらの値とクライアントです。 たとえば、クライアントは、同じ方法で同じステータスを持つフォルダーを表示する階層テーブル内のフォルダー間で視覚的に区別するためにフォルダーの状態を使用できます。 ビデオ、タグ付きのフォルダーを逆に強調表示されているフォルダーを表示できるし、わかりやすいアイコンが削除対象としてマークされているフォルダーを表示できる隠しフォルダーを非表示にできます。
  
31 (「0x80000000」からの「0x10000」) をこのプロパティの 16 ビットは IPM のクライアント アプリケーションで使用できます。 他のすべてのビットは、使用するため、MAPI ので予約されています上記の一覧で定義されていないものは、最初に 0 に設定する必要があり、変更されません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

