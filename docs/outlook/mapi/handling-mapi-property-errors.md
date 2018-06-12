---
title: MAPI プロパティのエラーを処理します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bb001d159141f70e9a82fa533e805f2a96b230ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800174"
---
# <a name="handling-mapi-property-errors"></a>MAPI プロパティのエラーを処理します。

**適用されます**: Outlook 
  
�S�ʓI�Ɏ��s�����܂��͐��������ꍇ�́A����ɂ́A���� **IMAPIProp**���@�́A�����I�Ȑ�����񍐂��܂��B 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps**は、少なくとも 1 つのオブジェクトに対して要求されたプロパティを取得できる場合に、部分的な成功を報告します。 **GetProps**は、MAPI_W_ERRORS_RETURNED の警告を返すと、 **lppPropArray**パラメーターで指定されたプロパティ値の配列で使用できないプロパティについての情報を配置することによって、部分的な成功を示します。 このアレイ上で使用できないプロパティのエントリには、**値**メンバーの**ulPropTag**メンバーと MAPI_E_NOT_FOUND またはその他の適切なエラー値のプロパティの型の PT_ERROR が含まれています。 たとえば、クライアントは、次の 3 つのプロパティを取得するために、フォルダーの**GetProps**メソッドを呼び出すし、3 番目では、メッセージ ストア プロバイダーは、PT_ERROR にプロパティの値の配列の 3 番目のプロパティの型と 3 番目の MAPI_E_NOT_FOUNDプロパティの値です。 
  
**IMAPIProp**���̕��@�ł́A�قȂ镔���I�Ȑ�����񍐂��܂��B�����̕��@�ł́AS_OK ��Ԃ�[SPropProblemArray](spropproblemarray.md)�\����̃G���[����z�u���ĕ����I�Ȑ�����񍐂��܂��B���\�b�h�̐����܂��͎��s�������ǂ����Ɋ֌W�Ȃ��f�[�^���܂܂�� **GetProps**�̃v���p�e�B�l�̔z��Ƃ͈قȂ�A���M�҂ɂ́A�G���[�ɂ��Ċw�K���o�^����Ă���ꍇ�ɂ̂݁A�G���[������ꍇ�ɂ݂̂����̕��@�Ńv���p�e�B�̖��̔z�񂪑��݂��܂��B���M�҂ɂ́A�G���[����o�^����L���� **SPropProblemArray**�|�C���^�[��w�肷��K�v������܂��B 
  
**SetProps**�A **DeleteProps**�A **CopyTo**�A�܂��� **CopyProps**����Ԃ��ꂽ�ꍇ�A�G���[�l�A�����̕����ł͂Ȃ��G���[������Ă��܂��B�v���p�e�B���z��ŁA�g�p�\�ȏꍇ�͖����ł��B�N���C�A���g���������\���ɕێ�����Ă���f�[�^�ɃA�N�Z�X����ɂ��Ă�\�����̂������悤�K�v������܂��B�K�؂ȉ�����[IMAPIProp::GetLastError](imapiprop-getlasterror.md)���܂��B 
  
**GetLastError**�́AWindows SDK �ɓ������O�̊֐��Ɏ��Ă��܂��B�߂�l�Ŏg�p�ł���ł͂Ȃ����ڍׂȃG���[�Ɋւ�����̑o����񋟂��܂��B���҂́A�O�̃G���[�������������ƂɊւ������Ԃ��܂��B���́AWin32 **GetLastError**�֐��̌Ăяo�����̃X���b�h�ɂ���Đ������ꂽ�G���[ ���|�[�g **IMAPIProp::GetLastError**����݂̃I�u�W�F�N�g�ɂ���Đ������ꂽ�G���[�̕񍐂ł��B�܂�A�N���C�A���g�ł́A���b�Z�[�W�� MAPI_E_NO_ACCESS �� **DeleteProps**��Ăяo���ꍇ�́A���̃��b�Z�[�W�͓ǂݎ���p�A **GetLastError**���b�Z�[�W����񋟂��ꂽ�f�[�^��Ԃ����Ƃ�����Ԃ���܂��B 
  
## <a name="see-also"></a>�֘A����

- [MAPI Property Overview](mapi-property-overview.md)

