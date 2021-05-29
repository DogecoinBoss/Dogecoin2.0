#
#  Panoramix v4 Oct 2019 
#  Decompiled source of bsc:0x3780E00D4c60887AF38345cCd44f7617dBFB10A0
# 
#  Let's make the world open source 
# 
#
#  I failed with these: 
#  - transferFrom(address _from, address _to, uint256 _value)
#  - unknown3bd5d173(?)
#  - unknown4549b039(?)
#  - transfer(address _to, uint256 _value)
#  - _fallback()
#  All the rest is below.
#

const unknown1694505e = 0x5ff2b0db69458a0750badebc4f9e13add608c7f
const unknown49bd5a5e = 0xd2390281d637a5dc27e3c4b1d03ac81e2aa425a2

def storage:
  owner is addr at storage 0
  stor1 is addr at storage 1
  unknownb6c52324 is uint256 at storage 2
  stor3 is mapping of uint256 at storage 3
  stor4 is mapping of uint256 at storage 4
  allowance is mapping of uint256 at storage 5
  stor6 is mapping of uint8 at storage 6
  stor7 is mapping of uint8 at storage 7
  stor8 is array of addr at storage 8
  totalSupply is uint256 at storage 9
  stor10 is uint256 at storage 10
  totalFees is uint256 at storage 11
  name is array of uint256 at storage 12
  symbol is array of uint256 at storage 13
  decimals is uint8 at storage 14
  unknown3b124fe7 is uint256 at storage 15
  unknown6bc87c3a is uint256 at storage 17
  stor19 is uint256 at storage 19 offset 8
  unknown4a74bb02 is uint8 at storage 19 offset 8
  unknown7d1db4a5 is uint256 at storage 20

def name(): # not payable
  return name[0 len name.length]

def totalFees(): # not payable
  return totalFees

def totalSupply(): # not payable
  return totalSupply

def decimals(): # not payable
  return decimals

def unknown3b124fe7(): # not payable
  return unknown3b124fe7

def unknown4a74bb02(): # not payable
  return bool(uint8(unknown4a74bb02))

def unknown5342acb4(addr _param1): # not payable
  require calldata.size - 4 >= 32
  return bool(stor6[addr(_param1)])

def unknown6bc87c3a(): # not payable
  return unknown6bc87c3a

def unknown7d1db4a5(): # not payable
  return unknown7d1db4a5

def unknown88f82020(addr _param1): # not payable
  require calldata.size - 4 >= 32
  return bool(stor7[addr(_param1)])

def owner(): # not payable
  return owner

def symbol(): # not payable
  return symbol[0 len symbol.length]

def unknownb6c52324(): # not payable
  return unknownb6c52324

def allowance(address _owner, address _spender): # not payable
  require calldata.size - 4 >= 64
  return allowance[addr(_owner)][addr(_spender)]

#
#  Regular functions
#

def renounceOwnership(): # not payable
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  log 0x728be007: owner, 0
  owner = 0

def unknown061c82d0(uint256 _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  unknown3b124fe7 = _param1

def unknown8ee88c53(uint256 _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  unknown6bc87c3a = _param1

def unknown437823ec(addr _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  stor6[addr(_param1)] = 1

def unknownea2f0b37(addr _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  stor6[addr(_param1)] = 0

def unknownc49b9a80(bool _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  Mask(248, 0, stor19) = Mask(248, 0, _param1)
  log 0x53726dfc: _param1

def lock(uint256 _expiration): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  stor1 = owner
  owner = 0
  unknownb6c52324 = _expiration + block.timestamp
  log 0x728be007 
  log 0x0 
  log 0x0 

def unlock(): # not payable
  if stor1 != caller:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  35,
                  0x6e596f7520646f6e27742068617665207065726d697373696f6e20746f20756e6c6f63,
                  mem[199 len 29]
  if block.timestamp <= unknownb6c52324:
      revert with 0, 'Contract is locked until 7 days'
  log 0x728be007: owner, stor1
  owner = stor1

def transferOwnership(address _newOwner): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  if not _newOwner:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  38,
                  0x734f776e61626c653a206e6577206f776e657220697320746865207a65726f20616464726573,
                  mem[202 len 26]
  log 0x728be007: owner, _newOwner
  owner = _newOwner

def unknownd543dbeb(uint256 _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  if not totalSupply:
      unknown7d1db4a5 = 0
  else:
      if _param1 * totalSupply / totalSupply != _param1:
          revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                      32,
                      33,
                      0x2e536166654d6174683a206d756c7469706c69636174696f6e206f766572666c6f,
                      mem[197 len 31]
      unknown7d1db4a5 = _param1 * totalSupply / 100

def approve(address _spender, uint256 _value): # not payable
  require calldata.size - 4 >= 64
  if not caller:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  36,
                  0x7345524332303a20617070726f76652066726f6d20746865207a65726f20616464726573,
                  mem[200 len 28]
  if not _spender:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  34,
                  0x7345524332303a20617070726f766520746f20746865207a65726f20616464726573,
                  mem[198 len 30]
  allowance[caller][addr(_spender)] = _value
  log Approval(
        address owner=_value,
        address spender=caller,
        uint256 value=_spender)
  return 1

def unknown3685d419(addr _param1): # not payable
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  if not stor7[addr(_param1)]:
      revert with 0, 'Account is already excluded'
  idx = 0
  while idx < stor8.length:
      mem[0] = 8
      if stor8[idx] != _param1:
          idx = idx + 1
          continue 
      require stor8.length - 1 < stor8.length
      require idx < stor8.length
      stor8[idx] = stor8[stor8.length]
      stor4[addr(_param1)] = 0
      stor7[addr(_param1)] = 0
      require stor8.length
      stor8[stor8.length] = 0
      stor8.length--
      stop

def decreaseAllowance(address _spender, uint256 _subtractedValue): # not payable
  require calldata.size - 4 >= 64
  if _subtractedValue > allowance[caller][addr(_spender)]:
      revert with 0, 
                  32,
                  37,
                  0x6b45524332303a2064656372656173656420616c6c6f77616e63652062656c6f77207a6572,
                  mem[165 len 27],
                  mem[219 len 5]
  if not caller:
      revert with 0, 32, 36, 0x7345524332303a20617070726f76652066726f6d20746865207a65726f20616464726573, mem[296 len 28]
  if not _spender:
      revert with 0, 32, 34, 0x7345524332303a20617070726f766520746f20746865207a65726f20616464726573, mem[294 len 30]
  allowance[caller][addr(_spender)] -= _subtractedValue
  log Approval(
        address owner=(allowance[caller][addr(_spender)] - _subtractedValue),
        address spender=caller,
        uint256 value=_spender)
  return 1

def increaseAllowance(address _spender, uint256 _addedValue): # not payable
  require calldata.size - 4 >= 64
  if _addedValue + allowance[caller][addr(_spender)] < allowance[caller][addr(_spender)]:
      revert with 0, 'SafeMath: addition overflow'
  if not caller:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  36,
                  0x7345524332303a20617070726f76652066726f6d20746865207a65726f20616464726573,
                  mem[200 len 28]
  if not _spender:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  34,
                  0x7345524332303a20617070726f766520746f20746865207a65726f20616464726573,
                  mem[198 len 30]
  allowance[caller][addr(_spender)] += _addedValue
  log Approval(
        address owner=(_addedValue + allowance[caller][addr(_spender)]),
        address spender=caller,
        uint256 value=_spender)
  return 1

def unknown2d838119(uint256 _param1) payable: 
  mem[64] = 96
  require not call.value
  require calldata.size - 4 >= 32
  if _param1 > stor10:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  42,
                  0x73416d6f756e74206d757374206265206c657373207468616e20746f74616c207265666c656374696f6e,
                  mem[206 len 22]
  idx = 0
  s = totalSupply
  t = stor10
  while idx < stor8.length:
      mem[0] = stor8[idx]
      mem[32] = 3
      if stor3[stor8[idx]] > t:
          _156 = mem[64]
          mem[64] = mem[64] + 64
          mem[_156] = 26
          mem[_156 + 32] = 'SafeMath: division by zero'
          if not totalSupply:
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _156 + 32]
                  idx = idx + 32
                  continue 
          else:
              _198 = mem[64]
              mem[64] = mem[64] + 64
              mem[_198] = 26
              mem[_198 + 32] = 'SafeMath: division by zero'
              if stor10 / totalSupply:
                  return (_param1 / stor10 / totalSupply)
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _198 + 32]
                  idx = idx + 32
                  continue 
          revert with 0, 'SafeMath: division by zero'
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 4
      if stor4[stor8[idx]] > s:
          _166 = mem[64]
          mem[64] = mem[64] + 64
          mem[_166] = 26
          mem[_166 + 32] = 'SafeMath: division by zero'
          if not totalSupply:
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _166 + 32]
                  idx = idx + 32
                  continue 
          else:
              _220 = mem[64]
              mem[64] = mem[64] + 64
              mem[_220] = 26
              mem[_220 + 32] = 'SafeMath: division by zero'
              if stor10 / totalSupply:
                  return (_param1 / stor10 / totalSupply)
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _220 + 32]
                  idx = idx + 32
                  continue 
          revert with 0, 'SafeMath: division by zero'
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 3
      _161 = mem[64]
      mem[64] = mem[64] + 64
      mem[_161] = 30
      mem[_161 + 32] = 'SafeMath: subtraction overflow'
      if stor3[stor8[idx]] > t:
          _168 = mem[64]
          mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
          mem[mem[64] + 4] = 32
          mem[mem[64] + 36] = 30
          idx = 0
          while idx < 30:
              mem[idx + _168 + 68] = mem[idx + _161 + 32]
              idx = idx + 32
              continue 
          mem[_168 + 68] = mem[_168 + 70 len 30]
          revert with memory
            from mem[64]
             len _168 + -mem[64] + 100
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 4
      _200 = mem[64]
      mem[64] = mem[64] + 64
      mem[_200] = 30
      mem[_200 + 32] = 'SafeMath: subtraction overflow'
      if stor4[stor8[idx]] <= s:
          idx = idx + 1
          s = s - stor4[stor8[idx]]
          t = t - stor3[stor8[idx]]
          continue 
      _217 = mem[64]
      mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
      mem[mem[64] + 4] = 32
      mem[mem[64] + 36] = 30
      idx = 0
      while idx < 30:
          mem[idx + _217 + 68] = mem[idx + _200 + 32]
          idx = idx + 32
          continue 
      mem[_217 + 68] = mem[_217 + 70 len 30]
      revert with memory
        from mem[64]
         len _217 + -mem[64] + 100
  if not totalSupply:
      revert with 0, 'SafeMath: division by zero'
  if t >= stor10 / totalSupply:
      if not s:
          revert with 0, 'SafeMath: division by zero'
      if not t / s:
          revert with 0, 'SafeMath: division by zero'
      return (_param1 / t / s)
  if not totalSupply:
      revert with 0, 'SafeMath: division by zero'
  if not stor10 / totalSupply:
      revert with 0, 'SafeMath: division by zero'
  return (_param1 / stor10 / totalSupply)

def balanceOf(address _owner) payable: 
  mem[64] = 96
  require not call.value
  require calldata.size - 4 >= 32
  if stor7[addr(_owner)]:
      return stor4[addr(_owner)]
  mem[0] = _owner
  mem[32] = 3
  if stor3[addr(_owner)] > stor10:
      revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                  32,
                  42,
                  0x73416d6f756e74206d757374206265206c657373207468616e20746f74616c207265666c656374696f6e,
                  mem[206 len 22]
  idx = 0
  s = totalSupply
  t = stor10
  while idx < stor8.length:
      mem[0] = stor8[idx]
      mem[32] = 3
      if stor3[stor8[idx]] > t:
          _161 = mem[64]
          mem[64] = mem[64] + 64
          mem[_161] = 26
          mem[_161 + 32] = 'SafeMath: division by zero'
          if not totalSupply:
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _161 + 32]
                  idx = idx + 32
                  continue 
          else:
              _203 = mem[64]
              mem[64] = mem[64] + 64
              mem[_203] = 26
              mem[_203 + 32] = 'SafeMath: division by zero'
              if stor10 / totalSupply:
                  return (stor3[addr(_owner)] / stor10 / totalSupply)
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _203 + 32]
                  idx = idx + 32
                  continue 
          revert with 0, 'SafeMath: division by zero'
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 4
      if stor4[stor8[idx]] > s:
          _171 = mem[64]
          mem[64] = mem[64] + 64
          mem[_171] = 26
          mem[_171 + 32] = 'SafeMath: division by zero'
          if not totalSupply:
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _171 + 32]
                  idx = idx + 32
                  continue 
          else:
              _225 = mem[64]
              mem[64] = mem[64] + 64
              mem[_225] = 26
              mem[_225 + 32] = 'SafeMath: division by zero'
              if stor10 / totalSupply:
                  return (stor3[addr(_owner)] / stor10 / totalSupply)
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 26
              mem[mem[64] + 68] = 'SafeMath: division by zero'
              idx = 32
              while idx < 26:
                  mem[idx + mem[64] + 68] = mem[idx + _225 + 32]
                  idx = idx + 32
                  continue 
          revert with 0, 'SafeMath: division by zero'
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 3
      _166 = mem[64]
      mem[64] = mem[64] + 64
      mem[_166] = 30
      mem[_166 + 32] = 'SafeMath: subtraction overflow'
      if stor3[stor8[idx]] > t:
          _173 = mem[64]
          mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
          mem[mem[64] + 4] = 32
          mem[mem[64] + 36] = 30
          idx = 0
          while idx < 30:
              mem[idx + _173 + 68] = mem[idx + _166 + 32]
              idx = idx + 32
              continue 
          mem[_173 + 68] = mem[_173 + 70 len 30]
          revert with memory
            from mem[64]
             len _173 + -mem[64] + 100
      require idx < stor8.length
      mem[0] = stor8[idx]
      mem[32] = 4
      _205 = mem[64]
      mem[64] = mem[64] + 64
      mem[_205] = 30
      mem[_205 + 32] = 'SafeMath: subtraction overflow'
      if stor4[stor8[idx]] <= s:
          idx = idx + 1
          s = s - stor4[stor8[idx]]
          t = t - stor3[stor8[idx]]
          continue 
      _222 = mem[64]
      mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
      mem[mem[64] + 4] = 32
      mem[mem[64] + 36] = 30
      idx = 0
      while idx < 30:
          mem[idx + _222 + 68] = mem[idx + _205 + 32]
          idx = idx + 32
          continue 
      mem[_222 + 68] = mem[_222 + 70 len 30]
      revert with memory
        from mem[64]
         len _222 + -mem[64] + 100
  if not totalSupply:
      revert with 0, 'SafeMath: division by zero'
  if t >= stor10 / totalSupply:
      if not s:
          revert with 0, 'SafeMath: division by zero'
      if not t / s:
          revert with 0, 'SafeMath: division by zero'
      return (stor3[addr(_owner)] / t / s)
  if not totalSupply:
      revert with 0, 'SafeMath: division by zero'
  if not stor10 / totalSupply:
      revert with 0, 'SafeMath: division by zero'
  return (stor3[addr(_owner)] / stor10 / totalSupply)

def unknown52390c02(addr _param1) payable: 
  mem[64] = 96
  require not call.value
  require calldata.size - 4 >= 32
  if owner != caller:
      revert with 0, 'eOwnable: caller is not the owne'
  if stor7[addr(_param1)]:
      revert with 0, 'Account is already excluded'
  if stor3[addr(_param1)]:
      mem[0] = _param1
      mem[32] = 3
      if stor3[addr(_param1)] > stor10:
          revert with 0x8c379a000000000000000000000000000000000000000000000000000000000, 
                      32,
                      42,
                      0x73416d6f756e74206d757374206265206c657373207468616e20746f74616c207265666c656374696f6e,
                      mem[206 len 22]
      idx = 0
      s = totalSupply
      t = stor10
      while idx < stor8.length:
          mem[0] = stor8[idx]
          mem[32] = 3
          if stor3[stor8[idx]] > t:
              _166 = mem[64]
              mem[64] = mem[64] + 64
              mem[_166] = 26
              mem[_166 + 32] = 'SafeMath: division by zero'
              if not totalSupply:
                  mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
                  mem[mem[64] + 4] = 32
                  mem[mem[64] + 36] = 26
                  mem[mem[64] + 68] = 'SafeMath: division by zero'
                  idx = 32
                  while idx < 26:
                      mem[idx + mem[64] + 68] = mem[idx + _166 + 32]
                      idx = idx + 32
                      continue 
              else:
                  _208 = mem[64]
                  mem[64] = mem[64] + 64
                  mem[_208] = 26
                  mem[_208 + 32] = 'SafeMath: division by zero'
                  if stor10 / totalSupply:
                      stor4[addr(_param1)] = stor3[addr(_param1)] / stor10 / totalSupply
                      stor7[addr(_param1)] = 1
                      stor8.length++
                      stor8[stor8.length] = _param1
                      stop
                  mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
                  mem[mem[64] + 4] = 32
                  mem[mem[64] + 36] = 26
                  mem[mem[64] + 68] = 'SafeMath: division by zero'
                  idx = 32
                  while idx < 26:
                      mem[idx + mem[64] + 68] = mem[idx + _208 + 32]
                      idx = idx + 32
                      continue 
              revert with 0, 'SafeMath: division by zero'
          require idx < stor8.length
          mem[0] = stor8[idx]
          mem[32] = 4
          if stor4[stor8[idx]] > s:
              _176 = mem[64]
              mem[64] = mem[64] + 64
              mem[_176] = 26
              mem[_176 + 32] = 'SafeMath: division by zero'
              if not totalSupply:
                  mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
                  mem[mem[64] + 4] = 32
                  mem[mem[64] + 36] = 26
                  mem[mem[64] + 68] = 'SafeMath: division by zero'
                  idx = 32
                  while idx < 26:
                      mem[idx + mem[64] + 68] = mem[idx + _176 + 32]
                      idx = idx + 32
                      continue 
              else:
                  _230 = mem[64]
                  mem[64] = mem[64] + 64
                  mem[_230] = 26
                  mem[_230 + 32] = 'SafeMath: division by zero'
                  if stor10 / totalSupply:
                      stor4[addr(_param1)] = stor3[addr(_param1)] / stor10 / totalSupply
                      stor7[addr(_param1)] = 1
                      stor8.length++
                      stor8[stor8.length] = _param1
                      stop
                  mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
                  mem[mem[64] + 4] = 32
                  mem[mem[64] + 36] = 26
                  mem[mem[64] + 68] = 'SafeMath: division by zero'
                  idx = 32
                  while idx < 26:
                      mem[idx + mem[64] + 68] = mem[idx + _230 + 32]
                      idx = idx + 32
                      continue 
              revert with 0, 'SafeMath: division by zero'
          require idx < stor8.length
          mem[0] = stor8[idx]
          mem[32] = 3
          _171 = mem[64]
          mem[64] = mem[64] + 64
          mem[_171] = 30
          mem[_171 + 32] = 'SafeMath: subtraction overflow'
          if stor3[stor8[idx]] > t:
              _178 = mem[64]
              mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
              mem[mem[64] + 4] = 32
              mem[mem[64] + 36] = 30
              idx = 0
              while idx < 30:
                  mem[idx + _178 + 68] = mem[idx + _171 + 32]
                  idx = idx + 32
                  continue 
              mem[_178 + 68] = mem[_178 + 70 len 30]
              revert with memory
                from mem[64]
                 len _178 + -mem[64] + 100
          require idx < stor8.length
          mem[0] = stor8[idx]
          mem[32] = 4
          _210 = mem[64]
          mem[64] = mem[64] + 64
          mem[_210] = 30
          mem[_210 + 32] = 'SafeMath: subtraction overflow'
          if stor4[stor8[idx]] <= s:
              idx = idx + 1
              s = s - stor4[stor8[idx]]
              t = t - stor3[stor8[idx]]
              continue 
          _227 = mem[64]
          mem[mem[64]] = 0x8c379a000000000000000000000000000000000000000000000000000000000
          mem[mem[64] + 4] = 32
          mem[mem[64] + 36] = 30
          idx = 0
          while idx < 30:
              mem[idx + _227 + 68] = mem[idx + _210 + 32]
              idx = idx + 32
              continue 
          mem[_227 + 68] = mem[_227 + 70 len 30]
          revert with memory
            from mem[64]
             len _227 + -mem[64] + 100
      if not totalSupply:
          revert with 0, 'SafeMath: division by zero'
      if t >= stor10 / totalSupply:
          if not s:
              revert with 0, 'SafeMath: division by zero'
          if not t / s:
              revert with 0, 'SafeMath: division by zero'
          stor4[addr(_param1)] = stor3[addr(_param1)] / t / s
      else:
          if not totalSupply:
              revert with 0, 'SafeMath: division by zero'
          if not stor10 / totalSupply:
              revert with 0, 'SafeMath: division by zero'
          stor4[addr(_param1)] = stor3[addr(_param1)] / stor10 / totalSupply
  stor7[addr(_param1)] = 1
  stor8.length++
  stor8[stor8.length] = _param1

