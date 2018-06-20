---
title: PidTagResourcePath の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803358"
---
# <a name="pidtagresourcepath-canonical-property"></a>PidTagResourcePath の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
サービス プロバイダーのサーバーへのパスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RESOURCE_PATH、PR_RESOURCE_PATH_A、PR_RESOURCE_PATH_W  <br/> |
|識別子:  <br/> |0x3E07  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティに含まれているパスは、ユーザーがリソースを検索する場所として推奨されるパスを表します。 これらのプロパティの定義は、特定のプロバイダーです。 などのスケジュール アプリケーションは、そのスケジュールのアプリケーション ファイルの推奨される場所を指定するのにこれらのプロパティを使用します。
  
メッセージングのユーザー プロファイルは、クライアント アプリケーションが、ネットワーク パスまたはネットワーク ドライブの文字のメッセージのユーザーに確認する必要があるないように、必要に応じてこれらのプロパティを提供します。
  
MAPI は、米国規格協会 (ANSI) 文字セットのファイル名でのみ動作します。 正規機器製造元 (OEM) 文字セットでファイル名を使用するアプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。
  
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

