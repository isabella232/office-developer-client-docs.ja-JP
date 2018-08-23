---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: fbf064201bf8d2733c3eea1e1a24f77b146a23c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564571"
---
# <a name="dnhier"></a>DNHIER

**適用されます**: Outlook 2013 |Outlook 2016 
  
階層サーバーからのダウンロード、[階層の状態をダウンロード](download-hierarchy-state.md)する時に完全な階層の同期の一部の情報です。 このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
>  [in]ダウンロード中に適切な動作を決定するフラグを設定します。 
    
   - DNH_OK
    
   - [in]ダウンロードが正常に完了しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
_pstmReserved_
  
> [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
_pxihc_
  
>  [out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。 **IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_cEntNew_
  
> [out]ローカル ストアに追加するフォルダーの数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
_cEntMod_
  
> [out]ローカル ストアを変更するフォルダーの数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
_cEntDel_
  
> [out]ローカル ストアから削除するフォルダーの数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
## <a name="see-also"></a>関連項目

- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md) 
- [MAPI �萔](mapi-constants.md)

