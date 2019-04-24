---
title: imapiprogress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270078"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションに進行状況のインジケーターを提供する progress オブジェクトを実装します。 進行状況インジケーターは、メッセージストア間でフォルダーをコピーするなど、操作の完了の割合を示すユーザーインターフェイスの表示です。 MAPI およびクライアントアプリケーションは、進行状況オブジェクトを実装し、サービスプロバイダーはそれらを使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |進行状況オブジェクト  <br/> |
|実装元:  <br/> |MAPI およびクライアントアプリケーション  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProgress  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[進行状況](imapiprogress-progress.md) <br/> |操作が完了した時点で進行状況のインジケーターを更新します。  <br/> |
|[getflags](imapiprogress-getflags.md) <br/> |進行状況の情報を計算する操作のレベルについて、progress オブジェクトからフラグ設定を返します。  <br/> |
|[getmax](imapiprogress-getmax.md) <br/> |進行状況の情報が表示される操作内のアイテムの最大数を返します。  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |プログレス情報が表示される[setlimits](imapiprogress-setlimits.md)メソッドの最小値を返します。  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |操作内の項目数の下限と上限を設定します。また、操作の進行状況に関する情報の計算方法を制御するフラグを設定します。  <br/> |
   
## <a name="remarks"></a>解説

MAPI には、潜在的に長い時間がかかる操作を実行する多くのメソッドの_lpprogress_パラメーターが含まれています。  _lpprogress_は、progress オブジェクトのクライアント実装を指します。 **imapiprogress**インターフェイスを実装するクライアントは、その実装をポイントするようにこのパラメーターを設定します。**imapiprogress**を実装していないクライアントは、パラメーターを NULL に設定します。 操作の処理中に進行状況インジケーターを表示するために、サービスプロバイダーは、クライアントによって提供される進行状況オブジェクト (使用可能な場合) または MAPI 実装 ( _lpprogress_が NULL に設定されている場合) を使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**Files**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiProgress および MapiProgress  <br/> |該当なし  <br/> |imapiprogress 設定が有効になっている場合、mfcmapi は、すべての関数に**imapiprogress**実装を渡します。この実装は、mfcmapi が呼び出す実装を受け入れます。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

