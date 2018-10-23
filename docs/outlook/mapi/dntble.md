---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391949"
---
# <a name="dntble"></a>DNTBLE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[テーブルの状態をダウンロード](download-table-state.md)中に、サーバーからフォルダーの内容をダウンロードするための情報です。 このダウンロード手順では、 Microsoft Exchange の増分変更の同期 (ICS) を使用します。 ICSの詳細については、[ICSの評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>メンバー

 _cEntNew_
  
> [out]ローカル ストアに追加されたアイテムの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
 _cEntMod_
  
> [out]ローカル ストアで変更されるアイテムの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
 _cEntRead_
  
> [出力]ローカル ストアで開封済みまたは未読にされているアイテムの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
 _cEntDel_
  
> [out]ローカル ストアで削除されるアイテムの数です。 ICS を使用してダウンロードしている間に Outlook がこの値を設定します。
    
## <a name="see-also"></a>関連項目



[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[DNTBL](dntbl.md)

