---
title: PidTagRemoteValidateOk の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803327"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>PidTagRemoteValidateOk の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロパティには、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドを呼び出してリモート ビューアーが許可されている場合 TRUE が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|識別子:  <br/> |0x3E0D  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、状態テーブルに表示される、トランスポートのパフォーマンスをある程度制御を提供しています。 それにアイドル状態のリモート ビューアーを指示する別の方法として検討できます。 TRUE に設定されている場合、リモートのビューアーは**IMAPIStatus::ValidateState**を何度でも呼び出すことができます。 FALSE の値は、リモートのビューアーが呼び出しを行うことはできませんを示します。 
  
トランスポート プロバイダーは、通常このプロパティを設定、動的に追加の呼び出しを無効にするトランスポート プロバイダーが実行する処理のための十分な量を持つ場合に false を指定する値を設定しています。 トランスポート プロバイダーが終了したら、さらに**IMAPIStatus::ValidateState**の呼び出しを行うクライアント アプリケーションを許可する場合は TRUE に値を設定します。 
  
## <a name="related-resources"></a>関連リソース

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

