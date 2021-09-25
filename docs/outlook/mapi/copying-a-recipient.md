---
title: 受信者のコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c9030d9341ba9aea0ce186ba4205242e5e65b1fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617049"
---
# <a name="copying-a-recipient"></a>受信者のコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つのコンテナーから別のコンテナーまたは同じコンテナーに 1 つ以上の受信者をコピーするには、まずターゲット コンテナーが変更可能なことを確認します。 変更可能なコンテナーは、AB_MODIFIABLE **(** [PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティPR_CONTAINER_FLAGSフラグを設定します。
  
1 つ以上のエントリを変更可能なコンテナーにコピーするには、宛先コンテナーの [IABContainer::CopyEntries メソッドを呼び出](iabcontainer-copyentries.md) します。 アドレス帳エントリのコピーには時間がかかる可能性があります **。CopyEntries** は、コピーするエントリのエントリ識別子の配列、ウィンドウ ハンドル、進行状況インジケーター、フラグのビットマスクの 4 つの入力パラメーターを受け入れる。 
  
ウィンドウ ハンドルと進行状況インジケーターは、アドレス帳プロバイダーによって操作の状態をユーザーに表示するために使用されます。 進行状況を表示する場合は  _、ulUIParam_ パラメーターの進行状況インジケーターの親ウィンドウのウィンドウ ハンドルを渡し  _、ulFlags_ パラメーターに AB_NO_DIALOG フラグを設定しない。 進行状況インジケーターの独自の実装がある場合は  _、lpProgress_ パラメーターの実装へのポインターを渡します。 指定しない場合は、NULL を渡します。 アドレス帳プロバイダーは、MAPI 進行状況インジケーターの実装を使用します。 
  
フラグのビットマスクは、進行状況インジケーターを表示するかどうか、および重複するエントリチェックの処理方法を示します。 進行状況インジケーターをAB_NO_DIALOGするフラグを設定します。 重複をCREATE_CHECK_DUP_LOOSEチェックするようにアドレス帳プロバイダーに指示する場合は、CREATE_CHECK_DUP_LOOSEフラグを設定し、重複のチェックを厳密に行CREATE_CHECK_DUP_STRICTフラグを設定します。 プロバイダーが重複CREATE_REPLACE判断した場合に、コピーされたエントリが既存のエントリに置き換わるかどうかを示すフラグを設定します。 
  
個人用アドレス帳 (PAB) コンテナーにコピーする場合、プロバイダーは各エントリのプロパティの一部またはすべてをコピーします。 MAPI はコンテナー コピー操作を実装するプロバイダーの要件を確立しないので、アドレス帳エントリでコピーされるプロパティの数と種類を想定することはできません。
  

