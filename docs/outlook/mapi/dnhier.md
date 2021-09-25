---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 7ec4de850efd7f92c065beb821a26a11aad1c440
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588141"
---
# <a name="dnhier"></a>DNHIER

**適用対象**: Outlook 2013 | Outlook 2016 
  
階層の完全同期の一部である[階層状態のダウンロード](download-hierarchy-state.md)中に、サーバーから階層をダウンロードするための情報です。 このダウンロード手順では、Microsoft Exchange の増分変更の同期 (ICS) を使用します。 ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
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

## <a name="members"></a>メンバー

_ulFlags_
  
>  [in] ダウンロード中の適切な動作を決定するフラグです。 
    
   - DNH_OK
    
   - [in] ダウンロードに成功しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
_pstmReserved_
  
> [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
_pxihc_
  
>  [out] 階層の増分変更のダウンロードをサポートする、**IExchangeImportHierarchyChanges** の階層インターフェイスのポインターです。 **IExchangeImportHierarchyChanges** の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
    
_cEntNew_
  
> [out] ローカル ストアに追加されたフォルダーの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
_cEntMod_
  
> [out] ローカル ストアで変更されるフォルダーの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
_cEntDel_
  
> [out] ローカル ストアで削除されるフォルダーの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
## <a name="see-also"></a>関連項目

- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md) 
- [MAPI 定数](mapi-constants.md)

