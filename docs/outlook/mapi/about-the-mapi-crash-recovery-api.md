---
title: MAPI クラッシュ回復 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: c429cee936390066499a85f9f130790c105481a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605238"
---
# <a name="about-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クラッシュ回復 API は、個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) 共有メモリの状態をチェックして、データが一貫性のある状態にあるか確認します。 一貫性のある状態の場合 [、MAPICrashRecovery](mapicrashrecovery.md) 関数は、開いている PST または OST からディスクにデータを移動し、PST または OST をロックし、データへの読み取りまたは書き込みアクセスを許可しません。 これにより、プロセスが終了するまでデータが一貫性のある状態を保ちます。 プロセスが終了する前に PST または OST が一貫性のある状態に保たれた場合、Microsoft Outlook 2013 と Microsoft Outlook 2010 が次のエラー メッセージを表示しないようにし、パフォーマンスの問題を回避できます。 
  
 **前回使用したデータ ファイルが正しく閉じなかったので、問題がチェックされています。チェックの進行中にパフォーマンスが影響を受ける可能性があります。**
  
この API は、次の機能を提供します。
  
定数:
  
- [MAPI �萔](mapi-constants.md)
    
関数
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>関連項目



[MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

