---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565859"
---
# <a name="dntble"></a>DNTBLE

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[テーブルの状態をダウンロード](download-table-state.md)する時にサーバーからフォルダーの内容をダウンロードするための情報です。 このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
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

## <a name="members"></a>Members

 _cEntNew_
  
> [out]ローカル ストアに追加された項目の数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
 _cEntMod_
  
> [out]ローカル ストアに変更された項目の数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
 _cEntRead_
  
> [out]アイテムの数は、読み取りまたはローカル ストア上の未読のマークです。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
 _cEntDel_
  
> [out]ローカル ストアで削除されたアイテムの数です。 Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。
    
## <a name="see-also"></a>関連項目



[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)
  
[DNTBL](dntbl.md)

