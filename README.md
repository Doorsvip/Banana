local _0x_g = game
local _0x_p = _0x_g.Players
local _0x_lp = _0x_p.LocalPlayer
local _0x_hg = _0x_g.HttpGet or function(s,u) return game.HttpGetAsync(s,u) end

local _0x_consts = {
    "\x73\x32\x52\x73\x50\x6D\x4B\x61\x77\x66\x41\x77\x32\x6F\x31\x50\x31",
    "\x42\x61\x6E\x61\x6E\x61\x20\x43\x61\x74\x20\x68\x75\x62",
    "\x20\x50\x72\x65\x6D\x69\x75\x6D",
    "https://i.ibb.co/Cp3t0j9B/1000002263.png",
    "\x6F\x62\x69\x69\x79\x65\x75\x65\x6D",
    "\x74\x79\x73\x6D\x20\x66\x6F\x72\x20\x75\x73\x69\x6E\x67\x20\x6D\x79\x20\x73\x63\x72\x69\x70\x74\x21",
    "\x57\x72\x6F\x6E\x67\x20\x6B\x65\x79",
    "\x68\x74\x74\x70\x73\x3A\x2F\x2F\x72\x61\x77\x2E\x67\x69\x74\x68\x75\x62\x75\x73\x65\x72\x63\x6F\x6E\x74\x65\x6E\x74\x2E\x63\x6F\x6D\x2F\x68\x6F\x61\x6E\x6E\x68\x61\x74\x7A\x2F\x53\x63\x72\x69\x70\x74\x2F\x72\x65\x66\x73\x2F\x68\x65\x61\x64\x73\x2F\x6D\x61\x69\x6E\x2F\x45\x5A\x53\x63\x72\x69\x70\x74\x2E\x6C\x75\x61"
}

local _0x_junk = function() local a=0 for i=1,math.random(80,250) do a=a+i end return a end
local _0x_dead = function() task.wait(math.random(0.01,0.05)) end
_0x_junk() _0x_dead()

local _0x_fetch = function(idx)
    local s = _0x_consts[idx] or ""
    return (s:gsub("\\x(%x%x)", function(h) return string.char(tonumber(h,16)) end)):gsub("\\(%d+)", function(d) return string.char(tonumber(d)) end)
end

if key == _0x_fetch(1) then
    getgenv().ScriptTitle          = _0x_fetch(2)
    getgenv().ScriptSubTitle       = _0x_fetch(3)
    getgenv().ScriptImage          = _0x_fetch(4)
    getgenv().ScriptAuthorName     = _0x_fetch(5)
    getgenv().ScriptAuthorSubTitle = _0x_fetch(6)
    
    local payload = _0x_hg(_0x_g, _0x_fetch(8))
    loadstring(payload)()
else
    pcall(function() _0x_lp:Kick(_0x_fetch(7)) end)
end

local _0x_trap = setmetatable({}, {__index = function() error("Integrity check failed - MoonSec V3") end})
pcall(_0x_trap)
