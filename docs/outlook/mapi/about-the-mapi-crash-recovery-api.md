---
title: MAPI クラッシュ回復 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321806"
---
# <a name="about-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クラッシュ回復 API は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックして、データが一貫性のある状態であることを確認します。 整合状態にある場合、 [mapicrashrecovery](mapicrashrecovery.md)関数は、open pst または ost からディスクにデータを移動し、pst または ost をロックし、データへの読み取りまたは書き込みアクセスを許可しません。 これにより、プロセスが終了するまで、データは一貫した状態に保たれます。 プロセスが終了する前に、pst または ost が一貫した状態になっていることを確認することにより、microsoft outlook 2013 と microsoft outlook 2010 が次のエラーメッセージを表示しないようにして、パフォーマンスの問題を回避することができます。 
  
 **データファイルが前回使用され、問題がないかチェックされているときに、データファイルが正常に閉じられませんでした。チェックが進行している間は、パフォーマンスが影響を受ける可能性があります。**
  
この API は、次の機能を提供します。
  
定数
  
- [MAPI �萔](mapi-constants.md)
    
関数
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>関連項目



[MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

