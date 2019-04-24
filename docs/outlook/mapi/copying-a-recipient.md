---
title: 受信者のコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333062"
---
# <a name="copying-a-recipient"></a>受信者のコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数の受信者を1つのコンテナーから別のコンテナーまたは同じコンテナーにコピーするには、最初にターゲットコンテナーが変更可能であることを確認してください。 変更可能なコンテナーは、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで AB_MODIFIABLE フラグを設定します。
  
1つまたは複数のエントリを変更可能なコンテナーにコピーするには、destination コンテナーの[IABContainer:: copyentries](iabcontainer-copyentries.md)メソッドを呼び出します。 アドレス帳エントリのコピーには時間がかかることがあるため、 **copyentries**は4つの入力パラメーターを受け取ります。コピーするエントリのエントリ識別子の配列、ウィンドウハンドル、進行状況インジケーター、およびフラグのビットマスク。 
  
ウィンドウハンドルと進行状況インジケーターは、ユーザーに対する操作の状態を表示するためにアドレス帳プロバイダーによって使用されます。 進行状況を表示する場合は、 _uluiparam_パラメーターで進行状況インジケーターの親ウィンドウのウィンドウハンドルを渡し、 _ulflags_パラメーターに AB_NO_DIALOG フラグを設定しないようにします。 進行状況インジケーターを独自に実装している場合は、 _lpprogress_パラメーターで実装へのポインターを渡します。 含まれていない場合は、NULL を渡します。 アドレス帳プロバイダーは、MAPI 進行状況インジケーターの実装を使用します。 
  
フラグのビットマスクは、進行状況のインジケーターを表示するかどうか、および重複するエントリチェックをどのように処理するかを示します。 AB_NO_DIALOG フラグを設定して、進行状況インジケーターを抑制します。 CREATE_CHECK_DUP_LOOSE フラグを設定して、アドレス帳プロバイダーに対して重複を緩やかにチェックするように指示します。また、より厳密な重複チェックを行うには CREATE_CHECK_DUP_STRICT フラグを設定します。 CREATE_REPLACE フラグを設定して、プロバイダーが重複していることを確認したときに、既存のエントリを上書きコピーします。 
  
個人用アドレス帳 (PAB) コンテナーにコピーすると、プロバイダーによって、各エントリのプロパティの一部またはすべてがコピーされます。 MAPI は、コンテナーコピー操作を実装するプロバイダーの要件を確立しないため、アドレス帳エントリと共にコピーされるプロパティの数と種類について前提条件を設定することはできません。
  

