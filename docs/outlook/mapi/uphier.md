---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 041ae867ff3a9cc9636ff1d93f9360576e455420
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804178"
---
# <a name="uphier"></a>UPHIER
 
**適用されます**: Outlook 
  
[階層の状態をアップロード](upload-hierarchy-state.md)する際にフォルダー階層を同期するための情報です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
> [in]フォルダー階層を同期するときの動作を変更するフラグを設定します。
    
  - UPH_OK
    
    - [in]アップロードが正常に完了しました。 クライアントでは、正常に情報をサーバーにアップロードした後、これを設定します。 このフラグを表示するには、時に、Outlook は、フォルダー階層の更新が必要なことを示す内部のブックキーピング情報をクリアします。 
    
    - クライアントは、アップロードが失敗した場合、HRESULT を渡します。
    
_pstmReserved_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
_iEnt_
  
> [out]*セント*で指定されたフォルダーの数の同期を追跡するためにインデックスを作成します。 
    
_セント_
  
> [out]同期が取られているフォルダーの数です。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)

