---
title: MAPI プロパティの取得
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417085"
---
# <a name="retrieving-mapi-properties"></a>MAPI プロパティの取得

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントまたはサービスプロバイダーがオブジェクトからプロパティを取得すると、そのオブジェクトはプロパティの値、型、および識別子を使用できるようになります。 
  
クライアントおよびサービスプロバイダーは、次のいずれかを呼び出すことによって、オブジェクトのプロパティを取得できます。
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
**GetProps**メソッドは、access の特殊なインターフェイスまたは代替インターフェイスを必要としない1つ以上のプロパティを取得するために使用されます。 これは、 **GetProps**で使用できるプロパティが、整数やブール値などの小さいことを意味します。 
  
 **複数のプロパティを取得するには**
  
1. 取得するプロパティの数を保持するのに十分な大きさの[SPropTagArray](sproptagarray.md)構造体を割り当てます。 
    
2. **SPropTagArray**構造体の**cvalues**メンバーを取得するプロパティの数に設定し、各**aulPropTag**メンバーを、可能であれば、いずれかのターゲットプロパティの識別子と種類に設定します。 種類が不明な場合は、PT_UNSPECIFIED に設定します。 型と識別子の両方が不明な場合は、 [imapiprop:: getproplist](imapiprop-getproplist.md)を呼び出すことによって、この情報を特定します。 **getproplist**は、オブジェクトでサポートされているすべてのプロパティを持つプロパティタグ配列を返します。 プロパティ名のみを使用できる場合は、関連付けられている識別子にアクセスするには、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出します。 
    
3. プロパティまたはプロパティを開くには、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出します。 
    
**openproperty**メソッドを使用すると、access の**IStream**や[IMAPITable](imapitableiunknown.md)などの代替インターフェイスを必要とする、より大きなプロパティを開くことができます。 **openproperty**は、通常、ラージ文字列、バイナリ、およびオブジェクトのプロパティを開くために使用され、一度に1つのプロパティしか開くことができません。 発信者は、入力パラメーターの1つとして必要な追加インターフェイスの識別子を渡します。 
  
**openproperty**の一般的な使用方法には、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を開くプロパティ (テキストベースのメッセージの本文を保持するプロパティ) **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) があります。OLE オブジェクトまたはメッセージの添付ファイル、および**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))。フォルダーまたはアドレス帳のコンテナーの内容の表を保持するプロパティ。 
  
プロパティによっては、 **openproperty**から別のインターフェイスが要求されます。 **IStream**は、プロパティデータをバイトストリームとして読み書きできるようにするインターフェイスです。通常、 **PR_BODY**へのアクセスに使用されます。 [IMessage](imessageimapiprop.md)または**IStream**のどちらかを使用して**PR_ATTACH_DATA_OBJ**にアクセスできます。 標準メッセージである埋め込みメッセージ添付ファイルは**IMessage**を使用しますが、TNEF 形式のメッセージでは**IStream**が使用されます。 **PR_CONTAINER_CONTENTS**は table オブジェクトなので、 [IMAPITable](imapitableiunknown.md)でアクセスします。
  
 **添付ファイルの PR_ATTACH_DATA_BIN プロパティを取得するには**
  
1. [openstreamonfile](openstreamonfile.md)関数を呼び出して、ファイルのストリームを開きます。 
    
2. メッセージの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティを取得します。 MAPI_MODIFY と MAPI_CREATE の両方のフラグを設定します。 
    
3. **STATSTG**構造体を割り当て、ファイルストリームの**IStream:: Stat**メソッドへの呼び出しに渡して、サイズを決定します。 ストリームのサイズを確認する別の方法として、 **IStream:: Seek**を STREAM_SEEK_END というフラグが付いています。 
    
4. ストリームの**IStream:: CopyTo**メソッドを呼び出して、ファイルのストリームから添付ファイルストリームにデータをコピーします。 
    
5. コピー操作が終了したら、 **IUnknown:: release**メソッドを呼び出して両方のストリームを解放します。 
    
**IStream**がプロパティアクセスに使用されている場合、一部のサービスプロバイダーは、プロパティのサイズを stream に自動的に送り返します。 MAPI_DEFERRED_ERRORS フラグを使用して**openproperty**を呼び出すと、プロパティのオープンとストリームサイズの戻りが遅延する可能性があります。 MAPI_DEFERRED_ERRORS フラグが設定された**openproperty** after でこの size を取得するために**IStream:: Stat**が呼び出された場合、この一連の呼び出しによってリモートプロシージャコールが強制的に実行されるため、パフォーマンスが影響を受けます。 パフォーマンスヒットを回避するために、クライアントは**openproperty**への呼び出しと**Stat**の間で任意の MAPI メソッドを呼び出すことができます。
  
[hrgetoneprop](hrgetoneprop.md)関数 ( **openproperty**など) は、一度に1つのプロパティを開きます。 **hrgetoneprop**は、ターゲットオブジェクトがローカルコンピューター上に存在する場合にのみ使用してください。 ターゲットオブジェクトがローカルで使用できない場合、 **hrgetoneprop**を繰り返し使用すると、複数のリモートプロシージャコールが発生し、パフォーマンスが低下することがあります。 
  
複数のプロパティを必要とする発信者は、ループで**hrgetoneprop**または**openproperty**を呼び出すか、 **GetProps**に対して1回の呼び出しを行うことができます。 **GetProps**の呼び出しは、より効率的です。 
  
> [!NOTE]
> セキュリティで保護されたプロパティは、 **GetProps**、 **hrgetoneprop**、または**getproplist**呼び出しの他のプロパティでは、自動的には使用できません。 セキュリティで保護されたプロパティは、プロパティ識別子を使用して明示的に要求する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

