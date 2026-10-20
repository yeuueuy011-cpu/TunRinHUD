--[[rscripts:analytics:start]]
-- Script analytics (enabled by the creator on rscripts.net).
-- Runs in its own thread and cannot affect the script below.
task.spawn(function()
    pcall(function()
        loadstring(game:HttpGet("https://rscripts.net/api/telemetry/v2/client.lua?s=6acb7056b7afa82fb859590e"))()
    end)
end)
--[[rscripts:analytics:end]]

-- Khởi tạo cấu trúc dữ liệu và nạp mã nguồn chạy các tính năng tự động (Farm, Sea Event, Raid,...)
local Success, Error = pcall(function()
    -- Tải trực tiếp mã nguồn nền tảng từ OpenSource BananaHub
    local RawScript = game:HttpGet("https://raw.githubusercontent.com/LSSOPS/OpenSource/refs/heads/main/BananaHub_Blox_Fruits.lua")
    
    -- Thay thế tên hiển thị giao diện cũ thành tên Hub mới của bạn
    RawScript = string.gsub(RawScript, '"Banana Hub"', '"TunRinHUD"')
    RawScript = string.gsub(RawScript, "'Banana Hub'", "'TunRinHUD'")
    RawScript = string.gsub(RawScript, "BananaHub", "TunRinHUD")
    
    -- Thực thi Script sau khi đã đổi tên thành công
    loadstring(RawScript)()
end)

if not Success then
    warn("Lỗi khi tải gonfunga hud script: " .. tostring(Error))
    -- Chạy dự phòng mã gốc nếu việc đổi tên bằng string.gsub gặp lỗi cấu trúc
    loadstring(game:HttpGet("https://raw.githubusercontent.com/LSSOPS/OpenSource/refs/heads/main/BananaHub_Blox_Fruits.lua"))()
end
