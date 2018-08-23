---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567154"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先フォルダーのエントリ ID が含まれています。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |msomapiutil.h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>Members

 **abFlags**
  
> オブジェクトを記述する情報を提供するフラグのビットマスクです。 詳細については、[エントリ ID](entryid.md)の構造体の**abFlags**フィールドの説明を参照してください。 
    
 **muid**
  
> ストア プロバイダーを識別する GUID。
    
 **ulVersion**
  
> **CONTAB_ENTRYID**構造体のバージョン番号です。 CONTAB_VERSION に設定する必要があります。 
    
 **ulType**
  
> 連絡先のエントリ ID の種類を表す整数。 次の値のいずれかを指定する必要があります。
    
|**名前**|**説明**|
|:-----|:-----|
|CONTAB_USER  <br/> |���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B  <br/> |
|CONTAB_DISTLIST  <br/> |�z�z���X�g �I�u�W�F�N�g�ł��B  <br/> |
   
 **ulIndex**
  
> 電子メールのプロパティのサブセットへのインデックスです。
    
 **cbeid**
  
> 連絡先アドレス帳内のこのエントリに関連付けられている取引先担当者のメッセージのエントリ id のサイズです。
    
 **abeid**
  
> 連絡先アドレス帳内のこのエントリに関連付けられている取引先担当者のメッセージのエントリ id です。
    
## <a name="remarks"></a>注釈

連絡先のアドレス帳は、アドレス帳を電子メール アドレスまたは fax 番号のいずれかを持つ連絡先フォルダー内のすべての連絡先アイテムを含むです。 連絡先のアドレス帳内の各エントリは、電子メール アドレスまたは fax 番号のいずれかに関連付けられます。 連絡先アイテムは、最大 3 つの電子メール アドレスを持つことができますので、3 つの fax 番号を 6 つまでのエントリに対応する連絡先のアドレス帳で連絡先アイテムを表すことができます。
  
連絡先のアドレス帳の目的は、ユーザーの連絡先フォルダーの連絡先に電子メール メッセージのアドレス指定をサポートします。 Contab32.dll を Microsoft Outlook 2010 と Microsoft Outlook 2013 でサポートされる連絡先のアドレス帳プロバイダーには。
  
**CONTAB_ENTRYID**構造体は、基になる MAPI 連絡先メッセージに表示される情報のサブセットをサポートします。 特定の連絡先のアドレス帳エントリが関連付けられている取引先担当者のメッセージを識別します。 
  
**Cbeid**と**abeid**フィールドは、 **ulType**フィールドの値は、CONTAB_DISTLIST または CONTAB_USER に設定されている場合にのみ有効です。 **UlType**フィールドの値を設定するには CONTAB_ROOT、CONTAB_SUBROOT、または CONTAB_CONTAINER、 [DIR_ENTRYID](dir_entryid.md)構造体を代わりに使用する必要があります。 
  
## <a name="see-also"></a>関連項目



[DIR_ENTRYID](dir_entryid.md)


[MAPI の構造](mapi-structures.md)

