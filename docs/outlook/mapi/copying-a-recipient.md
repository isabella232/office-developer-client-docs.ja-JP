---
title: 受信者のコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799836"
---
# <a name="copying-a-recipient"></a>受信者のコピー

  
  
**適用対象**: Outlook 
  
別の 1 つのコンテナー、または同じコンテナーには、1 つまたは複数の受信者をコピーするに最初の移行先コンテナーが変更可能なことを確認します。 コンテナーを変更することは、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティで、AB_MODIFIABLE フラグを設定します。
  
変更可能なコンテナーに 1 つまたは複数のエントリをコピーするには、移動先のコンテナーの[IABContainer::CopyEntries](iabcontainer-copyentries.md)メソッドを呼び出します。 アドレス帳のエントリをコピーできますが、時間がかかるため**CopyEntries**は 4 つの入力パラメーターを受け入れる: エントリをコピーする、ウィンドウ ハンドルを進行状況のインジケーター、およびフラグのビットマスクのエントリの識別子の配列。 
  
ウィンドウのハンドルと進行状況のインジケーターは、ユーザーに操作のステータスを表示するのには、アドレス帳プロバイダーによって使用されます。 進行状況を表示する場合は、 _ulUIParam_パラメーターの進行状況のインジケーターの親ウィンドウのウィンドウ ハンドルを渡すし、 _ulFlags_パラメーターでは AB_NO_DIALOG フラグを設定しません。 独自の実装の進行状況のインジケーターを使っている場合、実装、 _lpProgress_パラメーターへのポインターを渡します。 それ以外の場合は、NULL を渡します。 アドレス帳プロバイダーでは、MAPI の進行状況インジケーター実装を使用します。 
  
フラグのビットマスクを示し、進行状況のインジケーターを表示するかどうか重複したエントリを処理するかを確認します。 進行状況のインジケーターが表示されないようにするのには AB_NO_DIALOG フラグを設定します。 緩やかに重複データをチェックするのには、アドレス帳プロバイダーに指示するための CREATE_CHECK_DUP_LOOSE フラグまたは重複チェックの厳密な CREATE_CHECK_DUP_STRICT フラグを設定します。 エントリをコピーするのには CREATE_REPLACE フラグを設定しますは、プロバイダーは重複を決定するときに既存のエントリを置き換えます。 
  
個人用アドレス帳 (PAB) コンテナーにコピーする場合、プロバイダーは、各エントリのプロパティの一部またはすべてをコピーします。 MAPI は、コンテナーのコピー操作を実装するプロバイダーの要件を確立していない、ために、エントリをアドレス帳にコピーされるプロパティの種類と数についての前提条件を行うことはできません。
  

