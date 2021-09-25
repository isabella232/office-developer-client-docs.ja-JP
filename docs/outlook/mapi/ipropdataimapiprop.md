---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a590f5188d33d7fac0600f341d2c0fdef755b8e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579741"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトのプロパティのアクセスを取得および変更する機能を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|次のユーザーによって公開されます。  <br/> |プロパティ データ オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダーとクライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIPropData  <br/> |
|ポインターの種類:  <br/> |LPPROPDATA  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |1 つ以上のオブジェクトのプロパティのアクセス レベルと状態を設定します。  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。  <br/> |
   
## <a name="remarks"></a>注釈

**IPropData::IMAPIProp** インターフェイスは MAPI によって実装され、主に CreateIProp 関数を呼び出してこの実装にアクセスする [サービス プロバイダーによって使用](createiprop.md)されます。 
  
オブジェクトとプロパティのアクセス レベルの詳細については、「オブジェクトとプロパティの [アクセス許可」を参照してください](permissions-for-mapi-objects-and-properties.md)。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

