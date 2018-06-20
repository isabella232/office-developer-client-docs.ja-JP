---
title: MAPI �G���[�ۗ̕�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e2b091fa21dae4a1a8da23954d5f998010483da1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799884"
---
# <a name="deferring-mapi-errors"></a>MAPI �G���[�ۗ̕�

  
  
**適用されます**: Outlook 
  
�C���^�[�t�F�C�X�̂������̕��@�ł́A���̓p�����[�^�[�Ƃ��� MAPI_DEFERRED_ERRORS �t���O��������܂��B���̃t���O���ݒ肳��Ă���ꍇ�A���@���Ȃ��l�̒���ɖ߂�ɂ͌�ŁA�Ăяo���̌��ʂ�m�蔭�M�҂ɂ��Ƃ��ł��܂��B
  
サービス プロバイダーには、高速に処理することを複雑なメソッドの実装では、エラーを保留します。 多くの要求を処理し、それぞれの値を返すのではなくエラーを遅延させることは、サービス ・ プロバイダーにバンドルされているへの呼び出しを使用できます。 一度に多数の要求を処理パフォーマンスを向上させるため、ネットワーク トラフィックの削減します。 エラーを保留することは、呼び出しを削除またはコピーのプロパティは、非常に時間のかかる操作をすることができます便利です。 
  
�T�[�r�X �v���o�C�_�[���G���[�Ɋ֌W�Ȃ�����A�ۗ��N���C�A���g��Ăяo���Ƃ� MAPI_DEFERRED_ERRORS �t���O��ݒ肷�邾���ŏ����ł���x�������Ȃ��A�܂��� MAPI_E_TOO_COMPLEX ��擾���܂��B�قƂ�ǂ̃N���C�A���g�́A�ʘb�����s���邱�Ƃ�����ߐ헪�Ƃ��ăG���[��ۗ�����K�v������܂��B 
  
MAPI_DEFERRED_ERRORS を設定するフラグは、返される情報は、予定時刻ではなく、いつでも配信できるという点では、実装を処理するクライアントのエラーを変更します。 何もそれについて、または元の要求に関するデータが利用できなくすることが遅すぎる場合に返されるエラーが発生することができます。 などのクライアントは、MAPI_DEFERRED_ERRORS のセットを使用して削除されたフォルダーを開くには、 **IMsgStore::OpenEntry**を呼び出す、クライアントはわからない問題のフォルダーのプロパティのいずれかを取得するために、 **IMAPIProp::GetProps**の呼び出しが行われるまでです。 **GetProps** MAPI_E_NOT_FOUND を返します。 
  
## <a name="see-also"></a>�֘A����



[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)

