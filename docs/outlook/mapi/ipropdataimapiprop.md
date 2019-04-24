---
title: ipropdata imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279543"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトのプロパティのアクセスを取得および変更する機能を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|公開者:  <br/> |プロパティデータオブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービスプロバイダおよびクライアントアプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIPropData  <br/> |
|ポインターの種類:  <br/> |lppropdata  <br/> |
|トランザクションモデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B  <br/> |
|[hrsetpropaccess](ipropdata-hrsetpropaccess.md) <br/> |1つ以上のオブジェクトのプロパティのアクセスレベルと状態を設定します。  <br/> |
|[hrgetpropaccess](ipropdata-hrgetpropaccess.md) <br/> |�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B  <br/> |
|[hraddobjprops](ipropdata-hraddobjprops.md) <br/> |オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。  <br/> |
   
## <a name="remarks"></a>解説

**ipropdata:: imapiprop**インターフェイスは MAPI で実装されており、主に、 [createiprop](createiprop.md)関数を呼び出してこの実装にアクセスするサービスプロバイダーによって使用されます。 
  
オブジェクトおよびプロパティのアクセスレベルの詳細については、「[オブジェクトおよびプロパティのアクセス許可](permissions-for-mapi-objects-and-properties.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

