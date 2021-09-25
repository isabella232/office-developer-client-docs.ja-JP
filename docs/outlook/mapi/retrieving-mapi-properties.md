---
title: MAPI プロパティの取得
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 8c52f8a6768f43190bff86c8fe71c884102a4c91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624315"
---
# <a name="retrieving-mapi-properties"></a>MAPI プロパティの取得

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントまたはサービス プロバイダーがオブジェクトからプロパティを取得すると、オブジェクトはプロパティの値、型、識別子を使用できます。 
  
クライアントとサービス プロバイダーは、次のいずれかを呼び出すことによって、オブジェクトのプロパティを取得できます。
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
**GetProps メソッドは**、アクセスに専用または代替インターフェイスを必要としない 1 つ以上のプロパティを取得するために使用されます。 これは **、GetProps** で使用できるプロパティが小さいことを意味します (整数値やブール値など)。 
  
 **複数のプロパティを取得するには**
  
1. 取得するプロパティの数を保持するのに十分な大きい [SPropTagArray](sproptagarray.md) 構造体を割り当てる。 
    
2. **SPropTagArray** 構造体の **cValues** メンバーを取得するプロパティの数に設定し、各 **aulPropTag** メンバーを、可能であればターゲット プロパティの 1 つの識別子と型に設定します。 型が不明な場合は、この型を [PT_UNSPECIFIED] に設定します。 型と識別子の両方が不明な場合は [、IMAPIProp::GetPropList](imapiprop-getproplist.md)を呼び出してこの情報を探します。 **GetPropList** は、オブジェクトのすべてのサポートされているプロパティを持つプロパティ タグ配列を返します。 プロパティ名のみを使用できる場合は [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を呼び出して、関連付けられた識別子にアクセスします。 
    
3. [IMAPIProp::GetProps を](imapiprop-getprops.md)呼び出して、プロパティまたはプロパティを開きます。 
    
**OpenProperty メソッドは**、アクセスに **IStream** や [IMAPITable](imapitableiunknown.md)などの代替インターフェイスを必要とする大きなプロパティを開くのに使用されます。 **OpenProperty は** 通常、大きな文字列、バイナリ、およびオブジェクトのプロパティを開くために使用され、一度に 1 つのプロパティのみを開くことができます。 発信者は、入力パラメーターの 1 つとして必要な追加インターフェイスの識別子を渡します。 
  
**OpenProperty** の一般的な用途には、PR_BODY **(** [PidTagBody)](pidtagbody-canonical-property.md)を開く、テキスト ベースのメッセージの本文を保持するプロパティ **、PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)、OLE](pidtagattachdataobject-canonical-property.md)オブジェクトまたはメッセージ添付ファイルを保持するプロパティ、および **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)、フォルダーまたはアドレス帳コンテナーのコンテンツ テーブルを保持するプロパティがあります。 
  
プロパティに応じて **、OpenProperty** から別のインターフェイスが要求されます。 **IStream** は、プロパティ データをバイト ストリームとして読み取りおよび書き込みできるインターフェイスで、通常、プロパティ データにアクセス **PR_BODY。** [IMessage](imessageimapiprop.md)または IStream を使用して、IMessage または **IStream** **にアクセスPR_ATTACH_DATA_OBJ。** 標準メッセージである埋め込みメッセージ添付ファイルは **IMessage** を使用しますが、TNEF 形式のメッセージは **IStream を使用します**。 テーブル **オブジェクト** PR_CONTAINER_CONTENTS、IMAPITable を使用 [してアクセスされます](imapitableiunknown.md)。
  
 **添付ファイルのプロパティを取得PR_ATTACH_DATA_BINするには**
  
1. [OpenStreamOnFile 関数を呼び](openstreamonfile.md)出して、ファイルのストリームを開きます。 
    
2. メッセージの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイスで PR_ATTACH_DATA_BIN **(** [PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティを取得します。 パラメーター フラグとMAPI_MODIFYフラグMAPI_CREATEします。 
    
3. **STATSTG 構造を割** り当て、ファイル ストリームの **IStream::Stat** メソッドを呼び出してサイズを決定します。 ストリーム サイズを決定するもう 1 つの方法は、フラグを指定して **IStream::Seek** を呼び出STREAM_SEEK_END。 
    
4. ストリームの **IStream::CopyTo** メソッドを呼び出して、ファイルのストリームから添付ファイル ストリームにデータをコピーします。 
    
5. コピー操作が完了したら、両方のストリームを **IUnknown::Release** メソッドを呼び出して解放します。 
    
**IStream をプロパティ** アクセスに使用すると、一部のサービス プロバイダーはプロパティのサイズをストリームと一緒に自動的に送信します。 **OpenProperty を** MAPI_DEFERRED_ERRORSフラグで呼び出す場合、プロパティの開き方とストリーム サイズの戻り値が遅れる可能性があります。 MAPI_DEFERRED_ERRORS フラグが設定された **OpenProperty** の後にこのサイズを取得するために **IStream::Stat** が呼び出された場合、この一連の呼び出しによって余分なリモート プロシージャ呼び出しが強制的に行なうので、パフォーマンスが影響を受け取ります。 パフォーマンスのヒットを回避するために、クライアントは **OpenProperty** と Stat の呼び出しの間で MAPI メソッドを **呼び出します**。
  
[OpenProperty のような HrGetOneProp](hrgetoneprop.md) **関数は**、一度に 1 つのプロパティを開きます。 **HrGetOneProp** は、ターゲット オブジェクトがローカル コンピューターに存在する場合にのみ使用してください。 ターゲット オブジェクトをローカルで使用できない場合 **、HrGetOneProp** を繰り返し使用すると、複数のリモート プロシージャ呼び出しが発生し、パフォーマンスが低下する可能性があります。 
  
複数のプロパティを必要とする呼び出し元は、ループ内で **HrGetOneProp** または **OpenProperty** を呼び出すか **、GetProps** を 1 回呼び出すことができます。 **GetProps を 1 回呼** び出す方が効率的です。 
  
> [!NOTE]
> **GetProps、HrGetOneProp、または** **GetPropList** 呼び出しの他のプロパティでは、セキュリティで保護されたプロパティを自動的に使用できません。 セキュリティで保護されたプロパティは、プロパティ識別子を使用して明示的に要求する必要があります。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

