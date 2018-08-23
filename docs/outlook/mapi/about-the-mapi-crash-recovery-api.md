---
title: MAPI クラッシュ回復 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 34589860ed25f8236a343e16679c2e7a6bdd1e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799614"
---
# <a name="about-the-mapi-crash-recovery-api"></a>MAPI クラッシュ回復 API について

  
  
**適用対象**: Outlook 
  
MAPI クラッシュ回復 API では、個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態データが整合性の取れた状態であることを確認するためのメモリの共有を確認します。 コンシス テント状態の場合は、 [MAPICrashRecovery](mapicrashrecovery.md)関数は、開いているの pst ファイルまたは Ost からのデータをディスクに移動し pst ファイルまたは Ost をロックしの読み取りとデータへの書き込みアクセスが許可されません。 これにより、プロセスが終了するまでは、整合性の取れた状態にデータが残っています。 ことによって、pst ファイルまたは Ost 整合性の取れた状態でプロセスが終了する前に、Microsoft Outlook 2013 および Microsoft Outlook 2010 が次のエラー メッセージを表示することを防止し、パフォーマンスの問題を回避できます。 
  
 **データ ファイルを閉じませんでした正しく問題の最後に使用されていた、チェックされていること。チェックの実行中に、パフォーマンスは影響を受ける可能性があります。**
  
この API には、次のものが用意されています。
  
定数。
  
- [MAPI �萔](mapi-constants.md)
    
関数
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>関連項目



[MAPI クラッシュ回復 API を使用する](how-to-use-the-mapi-crash-recovery-api.md)

